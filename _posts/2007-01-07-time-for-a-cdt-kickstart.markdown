---
layout: post
title: Time for a CDT Kickstart?
date: '2007-01-07 23:28:00'
---


I subscribe to Google Alerts and get notifications whenever something new pops up mentioning the CDT. I’ve been seeing a lot of blog entries lately which is a cool sign that people are talking about the CDT and spreading the word. Unfortunately some of the comments deal with the difficulty of getting the CDT up and running, especially on Windows.

So I think it’s about time to do something about it. One thing I’ve wanted to do for a while now is to create a Windows installer that bundles up everything you need to start building applications with the CDT. As a product manager I used to work with said, “How do you call it an IDE when you don’t bundle a compiler with it?”

So my plan is to bundle the Eclipse Platform and the CDT run-times with the [MinGW](http://www.mingw.org/) gcc build tools and gdb debugger. I will bundle in [SDL](http://www.libsdl.org/), Simple Directmedia Layer, as a library to start building multimedia apps. I may look at bundling [wxWidgets](http://www.wxwidgets.org/) for building traditional GUI apps. I will also look at bundling a JRE so users can get Eclipse up and running with minimal effort, although I’m not sure if the Sun redistributable license will let me do this with an open source app and I’m not sure what other options I have.

Unfortunately a bunch of these components are GPL and LGPL so I won’t be able to release it from Eclipse itself given the IP rules. I’ll also need to figure out how GPL affects the package and it would be very disappointing if it prevents me from doing this. Sourceforge is probably the best place for this. I plan on using the Nullsoft Installer since it seems to have the most flexibility in any of the other free Windows installer technologies and is used by other open source projects such as MinGW itself.

So I’m interested in peoples’ opinions on this, if this is the right set of components for example. Is it worth my time putting together? The idea is to keep it simple so it doesn’t take me too much time to start and keep up to date. But I think it’ll be a boost to help new users get a start with the CDT, a Kickstart if you will.


