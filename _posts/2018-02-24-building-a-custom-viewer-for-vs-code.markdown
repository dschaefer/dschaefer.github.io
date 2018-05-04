---
layout: post
title: Building a Custom Viewer for VS Code
date: '2018-02-24 01:12:47'
tags:
- eclipse
---

I attended the online CheConf this week and was impressed by a few of the sessions. Now don't get me wrong, I still have reservations over the practicality of having your IDE in the cloud, at least in the embedded space where engineers tend to be more conservative. Certainly running tools inside docker containers makes sense and I believe all IDEs, cloud and desktop, need to be able to interface with them and Jeff from Red Hat is making good progress with that in the CDT. So we're not so different.

What did impress me from the sessions, though, is the progress we're starting to see with advanced visualizations using Web front ends. I was especially excited to see Mélanie from Obeo show Sirius there. And Silexica is doing some interesting visualizations of call graphs of C++ code with what I believe is D3.js. The charts you see come out of D3 are amazing, especially with animation. Being able to visualize complex systems this way will be a huge help to developers, epecially embedded engineers.

As I mentioned at the beginning of last year, I'm very excited about Electron as a desktop IDE platform. After playing around a bit on my own, I decided to give up and start working with one that's already well ahead, Visual Studio Code. Despite their claims to be focused on providing a great text editor, the community is working hard to make it a full fledged IDE. With the extensibility available today, you can do the same advanced visualizations we saw at CheConf as well as many other online tools.

I have created a demo of this capability as shown below. Click on the picture to see the github repo and the description in the README. It's dead simple but it shows how you can create a VS Code extension that renders in a webview whatever you would like with data fed from an embedded http server. It's a little weird, but once you get the plumbing done, you're on your way, and hopefully this demo can help you get started.

<a href="https://github.com/dschaefer/vscode-custom-viewer">
<img src="https://raw.githubusercontent.com/dschaefer/vscode-custom-viewer/18de5338b6bc6a5455efea521255dde6e6d28558/images/Capture.png" style="display: block; margin: 0 auto;">
</a>
<p></p>

There are many reasons why this move is important. There is so much momentum behind  web technologies with a seemingly endless line up of libraries on npm, to tutorials on the web, to people who know how to do this stuff. It only makes sense that we start to ride this wave as we did when the Eclipse IDE first came along. And, you know, fire this stuff up in a SWT Browser widget and you get that same experience and we can breath some new life into our old friend. It's an exciting future and it's a lot of fun trying to get there.