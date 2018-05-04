---
layout: post
title: Achieving Web Integration in the IDE with Electron
date: '2017-03-01 11:10:28'
tags:
- eclipse
---


It’s no secret that the modern developer’s favorite tool is Google. See a compile error you’ve never seen before, hell, cut and paste it into google.com and see if someone else has seen it and figured it out. It’s crazy how many times that works. <span style="font-size: 1rem;">That information sharing via blogs and forums makes the Internet an everyday part of a developer’s lives.</span>

And, of course, it doesn’t end there. The Web makes it very easy to build services around shared data and artifacts. We put our bugs in Bugzilla or JIRA, our code in Github or some other git repo on a server somewhere, run our builds in Jenkins, code reviews on Github or Gerrit. These web based tools are indispensable for developers.

Now, it’s not entirely without merit that you would want to put your IDE up on the Web as well. It could be just another tab in your browser that you already have open for these other tools. But people who know me know that I’m not sold that that’s a good answer for everyone. And I especially look to embedded developers who have boards hooked up to their development machines and have installed a bucket of tools, as old as they may be, that do a great job helping build software for those boards. That, and you’re laptop has a lot of power that you own and can do what you want with without sharing with dozens of other developers who want to do whatever they want to.

For me the best solution for now would be to find a way to merge all the great tools on the Web with all the great tools on your desk into seamless workflows where you forget where the tools reside and you just do. And that’s where my experimentation with [Electron](https://electron.atom.io) and my [Two IDE](https://github.com/dschaefer/eclipse-two) are showing a lot of promise. Let’s walk through an example with Github.

Have you ever opened up a Github page and clicked on the “Clone or Download” drop down? It’s pretty interesting that one of the choices is “Open in Desktop”. Click it in your browser and it takes you to a page to download Github’s developer tool. I’ve never used it but it sparked a similar idea I had for Two. It would be really cool to have a button that triggers the clone and sets it up in the IDE all in one click and a quick wizard for local settings.

![](/images/Screen-Shot-2017-03-01-at-10.31.42-AM.png)

So how would we go about that. Looking at the HTML source for the page, I was able to find the elements that created the Open In Desktop button. What I’d love to do is munge it somehow to say Open in Two IDE and add a click handler that would trigger the rest of the clone action.

One of the coolest things about Electron is that it has Chromium built in. And you can take full advantage of that and use the special features that Chromium has that the other browsers don’t. One of those is the webview element. It essentially creates a new rendering process that renders into an element managed by another process. I use it in Two to add a Github browser.

![](/images/Screen-Shot-2017-03-01-at-10.48.31-AM.png)

One of the attributes of the webview element allows you to specify a preload script. This script is run by the new rendering process before anything else in the new context. And this script has full access to the node.js environment. It lets you do some crazy things, like this:

import { remote } from 'electron'; window.onload = () => { const box = document.querySelector('.mt-2'); if (box) { const a: HTMLAnchorElement = <HTMLAnchorElement> box.children[0]; a.textContent = 'Open in Two IDE'; a.href = '#'; const input = box.previousElementSibling.children[2].children[0]; a.onclick = () => { remote.dialog.showMessageBox({ type: 'info', message: `Cloning ${input.getAttribute('value')}` }); }; } };

Now, this is TypeScript. But what I’m doing here is ‘require’ing the electron node module with the import statement which gives me access to the Electron remote API to call back to the main process. Whenever a page loads, I search the page for the element that contains the “Open in Desktop” element. I essentially hijack it and change the text and href and add a click handler to it. I get pretty sneaky looking for the URL for the clone by walking around the DOM a bit. I finally show that URL in a dialog box by calling the remote API to do that. Only the main process can open native dialogs.

Of course, I’ll eventually ask the user for a destination file path and any other arguments and then call the local git to make the clone happen and add it to the list of paths to show in the FIle Explorer. But for now, this is what I see:

![](/images/Screen-Shot-2017-03-01-at-11.01.48-AM.png)

Of course, you should be quick to point out that this is very fragile. If the Github gang redo the layout of the page, this breaks. But my theory is that if this type of integration becomes popular, you have a bit more leverage to go to them and create APIs, by having fixed classes or element ids that are more robust. Then any IDE trying to do this would benefit.

At any rate, this was a pretty early experiment that I haven’t spent a lot of time with. But it shows the path. By manipulating the content of the pages provided by web services, you can create workflows that span those services and the local development environment. And the user sees one tool. Click the Open in IDE button and it all magically gets set up and the IDE can switch automatically to the Code page to let you start working with it. Imagine what else you can do like this…


