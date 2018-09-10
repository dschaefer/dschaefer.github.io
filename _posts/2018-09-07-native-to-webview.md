---
layout: post
title: C++ and TypeScript - The Next Generation is Now
author: Doug Schaefer
date: 2018-09-10 00:00:00 -0400
tags:
- eclipse
---
We're coming up on the 10'th anniversary of one of my favorite EclipseCon memories, Eclipse Summit Europe 2008. Something about staying up until 5 a.m. local time with a bunch of messed up Canadians and Europeans who just didn't want to go to bed that make an event legendary. What made that special was probably the audience with a legend himself, Dave Thomas, who arguably started this all and who stayed right with us.

But it was his keynote, "Next Generation Embedded Software - The Imperative is Agility!" that I drew a lot of inspiration from. I can barely remember what it was about but he seemed to be bashing Java a lot so I had somewhat tuned it out. Until the last slide or so where he presented the alternative he controversially suggested would be the next generation: C++ and JavaScript. Wait, what?

I was probably the only person in the room who took that seriously. [It was the year that Google had introduced the V8 JavaScript virtual machine.](https://www.mediacurrent.com/blog/brief-history-googles-v8-javascript-engine/) I spent a little time after the conference figuring out how you'd use it with a C++ application and it definitely seemed plausible. What was missing was a user interface and that seemed like an enormous amount of work so I left it aside.

Fast forward a few years, we began to see people try and solve that problem by slapping node.js and browser together to create a desktop application framework. First, we had [NW.js](https://nwjs.io) who started with webkit but at some point switched to Chromium. Now we also have [Electron](https://electron.io) who have done the same but with more separation between node and Chromium to make it easier to keep up with releases of both, in theory.

Playing with Electron a couple of years ago I started to get the feeling that this vision was indeed coming soon, especially the first time I got Electron to load a C++ Node Addon. And now, I just used a C++ addon to solve a performance problem I was having in a VS Code extension (Electron incarnated as an IDE). That sealed it for me.

To show what I mean, I have taken the environment I'm using and created a really simple VS Code extension that has everything one would need to get started. It's dumb, but it implements an asynchronous native function to add two numbers and shows the results in a VS Code webview panel. It includes a bit of messaging framework to allow for type-safe(r) messaging between the webview and the extension. [As usual, it's available on my github to check out.](https://github.com/dschaefer/n2w-vscode-starter)

That was a bit of a long winded introduction, but I'll dive into the technical details for the rest of this article. Needless to say, I'm pretty excited about it.

## Believe Me, It Builds

Figuring out the cleanest way to build this thing and bundle everything together was the most challenging part, and probably what I'm most happy with. There are three different platforms at work and I am able to build them all with a single 'yarn compile'. And I'm able to work incrementally with minimal fuss, pretty much none, a watch, for for the extension and view and a simple incremental build for native on demand. And thanks to VS Code's TypeScript support and the clangd C++ language server, I find errors even before I build, as it should be.

### CMake

Let's start with the native side. Everyone who knows me from my work on the Eclipse CDT know I'm all about the CMake build tool these days. After years of working with Makefiles that model the system file by file, CMake lets you work at a higher level where you specify executables and libraries and dependencies between them. It takes care of the file level dependencies for you with a lot of magic, but good magic.

To build against the node.js APIs, you also need to download the header files, and for Windows, a library to build against. That's tricky to do, so I borrowed a few ideas from the interweb and created a NodeModule.cmake file under the CMake folder. It takes care of downloading the and extracting the necessary tar ball and sets up the dependencies to it. That makes the CMakeLists.txt file as simple as setting the Electron version for the tar ball, the output directory, and then defining your module.

``` cmake
set(ELECTRON_VERSION 2.0.5)
set(NODE_MODULE_OUTPUT_DIR ${CMAKE_SOURCE_DIR}/out)

include(NodeModule)
add_node_module(n2wNative native.cpp)
```

That places your module, n2wNative.node in this case, into a platform specific bin directory in the out directory of the project ready to import into the extension.

### Webpack

[Webpack](https://webpack.js.org/) seems to be the leading build framework for web applications. I also noticed with the latest VS Code release they are using it now with it's built-in extensions. Previously, I had a two step extension build, running webpack for client side and the TypeScript compiler for the extension. They both have file watchers but found the TypeScript one a bit flaky. So bringing them together into the same builder would make things a lot cleaner.

Webpack allows you to have multiple configs. I created one for the client side and one for the extension. The only real difference is the options for the TypeScript compiler to deal with the different modules systems between the browser and the extension which is running on node.js. I also chunked out the node_modules content for the clients since you are likely to have multiple of those.

The toughest issue I had was the 'require' loading the native module. It seems webpack tries to guess at location and changes the require to somewhere it thinks the module will be. But the whole idea of this module is that it's platform specific and it needs to calculate which platform it's on at run time. I finally ran into __non_webpack_require__ which is a hacky way to tell webpack to leave things alone. The TypeScript doesn't know about that magic so it needs to be declared.

``` typescript
declare function __non_webpack_require__(path: string): any;

export function add(x: number, y: number): Promise<number> {
    const native = __non_webpack_require__(`./${process.platform}/n2wNative`);
    return native.add(x, y);
}
```

The next issue I had to deal with was source maps. When I first got things running, VS Code with the Chromium debugger couldn't figure out my breakpoints. I managed to stumble across a magic command in the Debug Output view, .script, which showed a detail view of the source maps. Webpack uses a magic URL webpack:// in the source maps it seems to be causing the confusion. Luckily, I found out you can control that.

``` javascript
output: {
    path: path.resolve(__dirname, 'out'),
    filename: '[name].js',
    libraryTarget: 'commonjs',
    devtoolModuleFilenameTemplate: '[absolute-resource-path]'
},
```

devtoolModuleFilenameTemplate lets you manage the path used for your source file. I guess webpack is designed more for web apps where using the absolute path is weird.

## Time for a N-API

Node offers two API to hook up your C++ Addon, a scary one and a nice one. The scary one actually uses a lot of the V8 APIs and is heavy C++ and tends to tie you to a specific node release for some reason. Their newer simpler API introduce in version 8.0 is called N-API and thankfully VS Code finally switched to Node 8 in version 1.26. It's a C API and is very reminiscent of Java's JNI so I found it very easy to work with. It's marked experimental in Node 8 but I don't notice any major changes in version 10.

I didn't originally intend to go so native. I was working on a tool that scanned a gigabyte size binary memory mapped file extracting data. I started doing that in TypeScript using node Buffers and found the performance surprisingly good, under 3 seconds to do a complete scan. But then I added an else clause to the main if statement and the time hit around 15 seconds. Really? Did I disturb something in JIT that killed performance? How do you even predict how that's going to work.

Since I had written my own little memory map function using, I decided to rewrite the algorithm in C++ and ended up with around 1 seconds for the scan. Wow. Being a CDT guy, I know C++ and am pretty comfortable with it. And Modern C++ makes dealing with pointers pretty safe and collections fairly easy. For me, the performance gains were well worth it.

As I dug more into the features of N-API, I also discovered a hidden treasure. You can actually run your time consuming native algorithm on a worker thread and then use a JavaScript Promise to return the result when it finishes.

Basically, you create a struct to hold the arguments and result of the algorithm as well as the 'work' object the API gives you and a 'deferred' object that you use to resolve or reject the promise. That struct gets passed to a 'work' function that runs in a worker thread. When the work finishes a 'completed' function runs on the JavaScript main thread where you convert the result to a JavaScript value and send it out the promise through the deferred object. Easy, peasy, and pretty powerful.

I won't reproduce the whole file here, but check it out at [src/native/native.cpp](https://github.com/dschaefer/n2w-vscode-starter/blob/master/src/native/native.cpp). It's a bit wordy written in C but I imagine one could wrap it in some C++ classes and generics to make it easier.

## Playing it Safe

When you spend most of your life working in typed languages, first C++ then Java, the prospect of writing a serious app in a dynamically typed scripting language like JavaScript is a bit unsettling. Luckily I'm jumping into this as TypeScript is maturing. It has really helped me, especially as I learn both the VS Code API and the various npm packages I'm using thanks to the great IDE features you get with typed languages.

But there are two areas where you end up interacting with the raw JavaScript environment that you have to manage. The first is the native module. Most modules that you get off npm come with TypeScript definition files to make the integration easy. You have to provide something like that for the native module.

I already showed the TypeScript code to do this above. The require call returns a JavaScript object that you create in the module init native function. There are magic ways to give that object a type but I found it easier to start to just wrap it with a TypeScript function that manages loading the module and making the function call, at least for now.

The other area we need to manage is the communication channel between the extension and the code running in the webview. The webview extension API let's you bind a OnReceivedMessage callback that gives you the message as a JavaScript object. The webview client injects 'message' events into the window object where you can pick them up with a listener.

To make the messages type safe, I leveraged TypeScript's Discriminated Unions to declare message types in the [shared messages.ts file](https://github.com/dschaefer/n2w-vscode-starter/blob/master/src/common/messages.ts). On the client side, I created [a ServerPort class](https://github.com/dschaefer/n2w-vscode-starter/blob/master/src/view/ServerPort.ts) to manage the client side where I declared override methods to make posting messages type safe. The server side just has a switch statement where TypeScript figures out the type based on the case.

``` typescript
    async receiveMessage(request: Request) {
        switch (request.command) {
            case 'addRequest':
                this.postMessage({
                    command: 'addResponse',
                    token: request.token,
                    result: await add(request.x, request.y)
                });
                break;
        }
    }
```

That's the great thing about TypeScript. You still have the ability to do JavaScript when you need. But you have to come up with a strategy to minimize that surface area as much as possible.

## Challenges Ahead

Now that I have this running in Visual Studio Code, I don't see any reason why you couldn't use this architecture in other environments. It is just node.js and a browser in the end.

For example, I could simply get my tools running directly in Electron as a stand alone offering for people who don't want to use VS Code as an editor.

Web IDEs could also benefit. The Theia IDE promises to be compatible with VS Code extensions. It'll be interesting to try since this is probably the most complex extension I can think of. But other IDEs that have node.js as a server could also work this way.

But one thing is clear. I'm excited! Whether other tools developers will be as excited isn't as clear. Either way, I've found my next generation tools platform. It uses C++ and JavaScript/TypeScript. And that next generation is now.