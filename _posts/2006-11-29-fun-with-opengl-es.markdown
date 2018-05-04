---
layout: post
title: Fun with OpenGL ES
date: '2006-11-29 23:25:00'
---


I’ve got two young teenage boys and like a lot of other young teenage boys, they love video games. The computer geek in me, of course, made me wonder how the games were made. So I spent a fair amount of my hobby time a couple years ago learning a bit about the games industry and the technological challenges they face making games look great with limited resources. It was very interesting and if I was a few years (o.k., a lot of years) younger I would have considered a career change in that direction.

But I still poke my head into gaming technology once in a while, especially when I have an excuse to test the CDT on it. One thing that I ran across in my investigation into the needs of embedded developers is support for the OpenGL ES standard. This is a cut-down yet still pretty powerful version of the OpenGL standard that lies at the heart of video games like Doom 3 and the cool desktop effects you see with Mac OS X. The ES version is used on many embedded devices such as cell phones and PDAs.

[PowerVR](http://www.powervr.com/) is a chunk of 3D graphics silicon IP that is included in some pretty cool System-on-a-Chip (SoC) parts, often paired with Arm processors. I think you’ll see these chips popping up in many new and exciting places. But as this happens, they’ll need content to drive their 3D power. And that means a lot of people are going to need to learn how to program to the ES standard.

[Imagination Technologies](http://www.imgtec.com/) where PowerVR originates came up with a great way to get more people programming for their chips, a Windows OpenGL ES emulation environment. With this environment, you can program an OpenGL ES application and run it on your Windows box instead of having to fork out a lot of money for boards that have the PowerVR core until you get serious about it.

This is great example of why more embedded developers that I run into are excited about the Windows compiler and debugger support in the CDT I am working to deliver for CDT 4.0. With this environment you get a professional quality environment for Windows to build and debug your application with the emulator and then use the same development environment to work with the code as you polish it up for the end device. I’m really looking forward to getting this capability into developers hands so they can build some cool games. For the kids, you know…


