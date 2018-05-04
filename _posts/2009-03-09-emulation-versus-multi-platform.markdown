---
layout: post
title: Emulation versus Multi-Platform
date: '2009-03-09 22:56:00'
---


Over the last little while, when I could steal away a few minutes from my busy day job as of late, I’ve been thinking more about open platforms for handheld and set top consoles that makes good use of the 3D hardware that is becoming common place in these platforms. Of course, being open, I’m talking about open source and royalty free APIs like Linux and OpenGL and OpenGL ES.

I’ve been very excited about the LGPL’ing of the Qt C++ application framework. The programming paradigm is very clean and the library set is huge, including my favorite, the WebKit browser, and, of course, OpenGL support.

One angle I’ve been following is my other favorite piece of open source software, the qemu CPU emulator. The community is very active there and they’re are more and more platforms and hardware components being emulated making it a nice platform to play with some of the concepts I’m thinking of.

But the one critical piece missing is 3D hardware emulation. I would be great if someone could put that together, and given the comments on my previous blog entries, it would be very popular. I could do it, but I have the bigger picture in mind and have some other things I’d like to work on, in particular, a port of the Clutter concepts to Qt (and no, the QGraphicsView is close but not quite what I was thinking of).

Thinking about it tonight, it struck me. Since Qt is multi-platform and the tools I use, gcc and the CDT are multi-platform too, why don’t I just start this work on Windows using Wascana, the Eclipse CDT/mingw gcc package I am also trying to work on. I could even use the OpenGL ES emulation libraries that are out there to make sure these ideas work with OpenGL ES, another multi-platform component. And as my work here progresses, I will have the opportunity to use the same tools to make it work on real hardware.

It’s this type of environment that motivates my work on the CDT and what makes it so powerful. It’s time to put it to work for me.


