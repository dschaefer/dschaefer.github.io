---
layout: post
title: VirtualBox 2.0 gains an SDK
date: '2008-09-12 20:25:00'
---


When you’re an Eclipse developer like I am who is taking advantage of Eclipse’s cross-platform capabilities, you need to have a bunch of platforms to test your work on. The incredible growth of virtualization on the desktop over recent years has been a huge help for us who don’t necessarily want their offices filled with a dozen machines.

I’ve tried them all and settled on [VirtualBox](http://www.virtualbox.org/), which was recently bought by Sun, as my Windows Laptop solution (I use KVM on my Linux desktop box). It has the best handling of screen resizing I’ve seen and thanks to the great support for this in recent Linux distros, the window for the VM flows nicely into my daily workflow.

VirtualBox released their 2.0 version last week. The big news is support for 64-bit hosts and guests (yeah, old news for other solutions, especially given VirtualBox still doesn’t support SMP 🙁 ). But what caught my eye was that extra download labeled ‘SDK’. Nothing get’s me more excited than an extensible platform (well, there are some things…). So I was quick to unwrap their new gift.

The SDK mainly covers APIs they’ve exposed to build VM management tools, similar to libvirt that’s used on Linux platforms. It lets you create, configure, and launch VMs. Cool, and maybe it’ll lead to better UIs for this, mind you the one they have is already pretty good.

The more interesting part of this was the last chapter of the SDKRef PDF file. It talks about the mechanism they use to allow communication between the guest operating system and the host. It allows you to create your own drivers that communicate through a virtual PCI device to a shared library on the host. Now the header files weren’t shipped as part of the SDK, but they are part of the open source parts of VirtualBox. At least the doc shows you how. Very cool.

Now this comes to one of the most pressing things I wished virtualization could do, use the 3D graphic chips on the host. If I want to experiment with some of the ideas I have for 3D Linux UI frameworks, and still use Windows for my day job, I need something like that. And with this capability opened up for us to use, I can quickly imagine how I could get OpenGL calls from a guest OS out through this mechanism to the host OpenGL libraries. And I guess I’m not alone. In the list of built-in users of this mechanism is a mysterious service called VBoxSharedOpenGL.


