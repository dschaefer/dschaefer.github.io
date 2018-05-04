---
layout: post
title: GWT + Server-side Eclipse = W-IDE
date: '2009-07-30 10:11:00'
---


Someone once asked me why we break up things between ui plug-ins and core plug-ins. My theory was that we could eventually swap out the ui with something else. I didn’t really believe that at the time, and I’m not sure how well architected our CDT plug-ins are to allow that, but it sounded good.

So as I begin my journey down the road of web-based IDE’s it really struck me that this was the time to swap out the UI. My theory goes like this. Google are the experts at creating web applications (and you may disagree with that, but stick with me). They have a framework for building them called the Google Web Tooklit, GWT, which allows you to program your UI in Java which then gets compiled into JavaScript. And, they have a really cool RPC mechanism, again all in Java, that overlays Servlets. Hey, Equinox plus Jetty gives you Servlets. Why not swap out the Eclipse UI code with a GWT implementation that talks to our Core code using Servlets?

A big thanks goes out to Ian Bull who reminded me of the example project he created last year that shows how to use GWT with Equinox OSGi. I have extended that a little to call into the Eclipse workbench, right now calling Platform.getOS(). This is the start of my prototype web-based IDE using GWT as a front end to the Eclipse IDE Core parts. And I am pumped the deeper I get into it. Feel free to follow along as I check my prototype into [http://github.com/dschaefer/w-ide](http://github.com/dschaefer/w-ide). Feel free to fork that and join in the fun. (BWT, I need to show you the cool way I’m using git, stay tuned).

As Ian says, “GWT + OSGi is a great platform!” And I am starting to see why. It really is. So much so that it confirms my earlier conjecture that Equinox would be a great addition to Chrome OS and I hope Eclipse people are talking to Google people about that. Wouldn’t it be cool to see Equinox serving up local server pages, presenting a p2 install web UI to download and install bundles into your favorite mobile device. Yes, it would be cool.


