---
layout: post
title: Aliens, Go Home! VS Code-style!
author: Doug Schaefer
date: 2018-08-31 14:01:00 -0400
tags:
- eclipse
comments: true
---
<img src="https://cdtdoug.ca/images/aliens-vscode.png" style="display: block; margin: auto; height: 400px">

Looks ridiculous, doesn't it. There is a method to my madness though. Stick with me...

I make it no secret how enthusiastic I am about Visual Studio Code as an IDE platform. I have often commented on my desire to start building tools using web front end technologies (and not necessarily web back ends). I even prototyped an ["Eclipse Two"](https://cdtdoug.ca/2017/02/16/what-is-two-much-more-than-yet-another-eclipse-ide.html) that was built on Electron directly. In the end, the Microsoft Zurich team, who also happened to be former leaders at Eclipse, created something similar with a huge community and ecosystem of extensions and I jumped on the bandwagon.

Being a good code editor and debugger is one thing, in the end there's more to life as a developer than writing code. Often the systems we work with are more complicated than can be simply represented in text. We need graphics that can abstract away some of the gory details and make system behavior and relationships easier to understand. And that includes both ends, from modeling when creating the system, to tracing when trying to see what it's doing once we built it.

There's a number of ways you can do graphics in a web front end. The first one I considered was SVG. I like it because it's backed by a data model with API that will let you change properties programmatically. And it simply gives an object oriented approach to graphics. It's not all good though since those objects come with a price in memory and setup time. But if you keep the number of elements you create under a thousand or so, it's pretty quick.

The other advantage of being in the DOM is that React can handle SVG with it's virtual DOM. This speeds up rendering from changes to the underlying data model and automatically calculates that for you. It's one of the coolest things in React and why we use it for all our web UI work.

So I set off to google around for examples where people had done that and I quickly ran across an article series [Developing Games with React, Redux, and SVG](https://auth0.com/blog/developing-games-with-react-redux-and-svg-part-1). It's really cool and proves out my main thesis about handling changing data models. Games, of course, are all about changing data models!

 To complete the exercise, hooked up a simple VS Code extension that opened up a webview panel and ran the game in it. I rewrote most of it using TypeScript, since I refuse to give into the typeless world of JavaScript. I also switched over to MobX which some of my colleagues were using and it's much easier to deal with than Redux. The whole thing was a joy to work with.

 If you're interested, [I have pushed up my results to my GitHub repositories](https://github.com/dschaefer/aliens-vscode). It does look ridiculous running in VS Code. But it shows off the power of the platform. Running in a webview means you're running in a separate process from the rest of vscode so what ever you do there doesn't impact the rest of the IDE. From there, you can communicate back with your extension to allow it to interact with your environment and grab data from systems and files and feed back data for rendering. I can't wait to see where the community (and myself for that matter) take this architecture.