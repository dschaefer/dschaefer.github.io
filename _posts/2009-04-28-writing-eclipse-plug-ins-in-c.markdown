---
layout: post
title: Writing Eclipse Plug-ins in C++
date: '2009-04-28 22:16:00'
---


Well, not the entire plug-in. But I thought that would get your attention.

After spending a while mulling around with embedded Linux and Qt and qemu and thinking about OpenGL ES and how I’d build a handheld console or set top box that had a 3D graphical environment using something like Clutter, I’m now trying to figure out what kind of tools you’d need for such a world where 3D graphics was common place.

That led me back to something I tried a couple of years ago, trying to get OpenGL rendering in Eclipse. The idea was to provide a complete tool suite for building 3D games in Eclipse. We have C/C++ covered with the CDT. You might also want some 3D modeling tools for building characters and scenes. Why couldn’t that be in the Eclipse environment as well. Yes, these are usually done by different people, but I’m thinking of the small, independent developer shops where that may not be true.

The OpenGL canvas widget in SWT makes this pretty easy. I installed the LWJGL library that allows you to make OpenGL calls in Java and I got the Snippet that draws a torus spinning around in an SWT window running. Very cool.

But as I often mentioned here, I “hate” Java (well, it’s pretty much a love/hate relationship since I still pick it for my day job on Eclipse technologies). I want to have the option of using native CPU capabilities like SIMD instructions you get with the SSE family instructions. So I’d prefer to do as much as possible in C++.

So I did that. I got rid of the LWJGL code and replaced it with my own native library that implemented an init, resize, and draw routine. Essentially this is all the code needed to render into the canvas and you can do the rest with a few Java calls to set the current context and to swap the buffers. Very very cool. Now to get this running in an Eclipse editor and we’re off to the races.

Here’s a snapshot of what I have so far. And yeah, it looks like the LWJGL version, but, trust me, all the OpenGL code is in C++ behind the three native methods:

[![](http://2.bp.blogspot.com/_X6Gz24BqUwI/SffKvilaUuI/AAAAAAAAAAw/jcLizeN3WtU/s400/Screenshot-SWT+Native+GL+Example+.png)](http://2.bp.blogspot.com/_X6Gz24BqUwI/SffKvilaUuI/AAAAAAAAAAw/jcLizeN3WtU/s1600-h/Screenshot-SWT+Native+GL+Example+.png)


