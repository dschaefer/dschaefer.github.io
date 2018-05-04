---
layout: post
title: Fun with Qemu/Qt
date: '2009-04-13 00:15:00'
---


Just for fun (and maybe profit), I thought I’d try and get Qt running on the mini ARM Linux setup that I used for my tutorial at EclipseCon. Low and behold, all I had to do was build it with the compiler I got from CodeSourcery for ARM and it worked!

Now there isn’t a whole lot of magic here. It’s using the Linux framebuffer device that draws to the screen. I’m not sure how it would look on a real device but it looked might fine on qemu. Here’s a snapshot of it running on my laptop, which is now solidly Fedora. It’s running the browser demo app and has loaded my blog just before I posted this. It took a little while to load and render, but again, it looked pretty good.

[![](http://2.bp.blogspot.com/_F9-xsix-Zh4/SeLKwu77wII/AAAAAAAAACM/UMqP4_5QJPc/s400/Screenshot-QEMU.png)](http://2.bp.blogspot.com/_F9-xsix-Zh4/SeLKwu77wII/AAAAAAAAACM/UMqP4_5QJPc/s1600-h/Screenshot-QEMU.png)

Having gotten this far, I start to wonder how much better it would be if I had OpenGL ES emulation in qemu. Would it be faster? Curiosity might kill this cat…


