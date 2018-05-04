---
layout: post
title: Windows as a host for Linux development?
date: '2008-10-16 23:55:00'
---


Here’s something I’m trying to decide as I work through the ultimate development environment for a Linux based “OpenConsole” (and to be clear, I’m talking about set top box class consoles, not mobile). As I mentioned in previous blog entries, I’ve figured out how to extend qemu to do OpenGL calls on the host and present a PCI interface to the guest to make those calls. All I need is a Linux driver and user space library to use that interface and present the OpenGL (or OpenGL ES) interface to applications that can do games, or what have you.

I figure Linux is a natural host development environment for the device driver. You need to reuse the kernel build system to build it and from what I understand, that build system doesn’t work on Windows, not even with Cygwin. So that’s a lock, and I can use the Linux version of CDT to build it.

But when it comes to applications, I am wondering how many developers would prefer to use Windows as their development host. From what I understand (again, and I keep guessing here), most game development is done on Windows, even when targeting the “closed” consoles. Actually, XBOX development is obviously done on Windows. But I believe the others have Windows hosted SDKs and tools as well.

However, as with device drivers, Linux should be an obvious choice for application development targeting Linux. This is especially true when targeting PC-type platforms since the host tool chain can actually be used to target the console, and even more true when you’re actually using the same run-time lineup.

I get the feeling that there’s more to life than writing your Linux targeted application. If, as the developer, you’re still relying on a lot of Windows tools or you just plain prefer Windows as a work environment, you would probably want to write your application on Windows as well.

It’s funny how we sometimes forget history and the fact that we abandoned our Unix environments for Windows because it had much better tools. And as I (and many others) have discussed, Linux hasn’t caught up yet to make us want to go back. So I firmly believe that Windows is an expected host development environment for Linux development, especially embedded. And with the help of gcc’s cross compilation abililty and the gcc support in the CDT, it’s shouldn’t be that hard to put together.


