---
layout: post
title: A cool multi-platform CDT use case
date: '2008-09-20 10:08:00'
---


I previously blogged about the VitualBox SDK and the capability it provides to build some really interesting emulation environments, 3D graphics being the one I’m most interested in at the moment. And this is something I’m seeing in the embedded industry a lot lately. Hardware is expensive. These boxes we have on our desks are very powerful and relatively pretty cheap. Being able to emulate hardware during the software development phase of a project gives the developer the ability to get his code up and running much earlier.

So looking at how I’d build an emulator for a Linux set-top box that had 3d graphic capabilities, it quickly became apparent again how the multi-platform capabilities of the CDT gives me an top class C/C++ IDE to do work on all of the components. Here’s what they would include:

- The 3D graphics emulator is a shared library that VirtualBox loads and, of course, runs on the host. I would start with doing it on Windows since that’s my main environment. I’d use either MinGW gcc or the Visual C++ compiler. CDT has support for building both but only debugging with gcc at the moment. But shared library debugging on Windows has always been trouble with the CDT so that might not be important. In the long run, I’d probably also want to do this for a Linux host environment.
- The box would run Linux, of course. I’d need to be able to build the drivers that talk to the emulated 3d graphics thing. And I’d need to be able to build a bootable image with the kernel and the drivers and any core utilities I would need. Again CDT comes to the rescue, but I’d probably pick a commercialized version that automates Linux kernel development such as Wind River’s Linux platform builder. And I’d have to use my Ubuntu development environment on VirtualBox to run it since Linux is the only environment that really supports building the Linux kernel.
- For the actual user space programs that provide the content, I can use the CDT again. This is the main environment that is used by the community building stuff for the box. gcc’s great cross compilation support makes it less obvious whether you’d do this on Windows or Linux. Linux would be a favorite since you can easily share your development workspace with the target using NFS. Something not as easy on Windows.

For me, this is the big advantage of the CDT. You have yourself doing host and target development on Windows and Linux, and even Mac if you wanted to, all using the same tools that have the same UI and keyboard shortcuts. Now, where’s that cloning machine so I can actually go build this thing…


