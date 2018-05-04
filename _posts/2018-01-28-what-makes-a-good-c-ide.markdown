---
layout: post
title: What makes a good C++ IDE?
date: '2018-01-28 18:31:34'
tags:
- eclipse
---

When I started working on C code many years ago, I was a big fan of emacs. It didn't have the weird modes that vi did. You just typed and code showed up. emacs has a rich extension system, if you don't mind writing LISP code, and soon we had fancy features such as running builds and navigating through compile errors. There's even a gdb integration that gives you what you need to debug your program. And then along came ctags and we started getting source navigation.

But what was good for C started to fade with C++. We also started bringing in code coverage and profiling tools and even modeling and code generation tools. Simple editors like emacs couldn't keep up. We needed much more powerful platforms that provided a richer environment for tools as well as the promise of standard interfaces that allowed us to integrate tools to provide functionality greater than the whole. The IDE was born.

But somewhere along the way it seems we failed. We didn't provide enough value that warranted the opinionated structures that IDEs enforce that enable the standard APIs to work. As I've stated many times, we have paid dearly with Eclipse trying to force C/C++ projects into the Eclipse resource system. What is a project in C/C++ world? Are projects the root of a recursive make tree, or the individual nodes that represent executable things and libraries? Neither works well, especially in complex systems embedded systems developers are building.

So after years of trying to convert die hards and working hard to support those who want to use our IDEs, we need to take a step back try again. Get back to emacs, or more modern editors like Visual Studio Code, and see how we can bring our users forward again. This time we need to do it in a way that doesn't enforce a paradigm on them yet provides a path back towards the valuable features we can provide through integration.

Anyway, that was a long preamble towards the real topic of this post, remembering what made CDT successful and providing at least that first step forward. What is the minimal feature set that meets expectations of today's developers. As I was using Visual Studio Code to hack Visual Studio Code, you get a real sense of what that is. You also get a good sense at what's missing from these editors. 

First of all is source navigation, being able to control click to find definitions of symbols and to be able to search for references to them. And, of course, along with that comes content assist. I spent most of my early years on CDT figuring out how to do this properly and quickly. For those that remember, the quickly took a long time and in the end exchanging perfect answers for speed was our path to success. To make this work we hand built C and C++ parsers that referenced a symbol database called the index. You also need to know the toolchain and build system to know how the code is built to do a reasonable job at it. Integration with the build system is a must.

It's hard to imagine how editors like VS Code can be a good CDT replacement without replicating the magic. I'm not convinced the current front runner clangd and it's use of the clang parser which has perfection as it's number one requirement, will get us there without a lot of hacking. And editors usually don't deal with builds other than to invoke them and give you error navigation to feed it the info it needs.

And I'm not even touching on launching where you really need to match build configs with launch configs to make sure launches do what you want. So while editors are all the rage right now because they are lightweight and flexible, users still expect them to more than the editors of old. It will be an interesting challenge for those who go that road to walk that balancing line. If you get it right though, I can imagine a lot of happy users.