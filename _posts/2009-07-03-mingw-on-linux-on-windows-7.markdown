---
layout: post
title: MinGW on Linux on Windows 7???
date: '2009-07-03 13:54:00'
---


My Windows/Linux world has gotten a whole lot more complicated in the last few days, but I’m really liking how it’s set up now.

As I mentioned in my blog entry on multi-target Makefiles, I am using Fedora 11’s mingw cross compiler along with gcc’s multilib support and am building the little C++ project I’m working on at work for both 32 and 64-bit Linux as well as Windows all in the same Makefile and all on every build of my CDT project. That is extremely handy and I’ve already fixed a problem early where there is a mismatch between the linux and mingw environments, no strndup on mingw, and was able to do so without switching machines.

This is awesome and I’ll be able to produce executables for all three of these platforms for testing all in one shot. Kudos to the Fedora folk for providing first class support for mingw cross compilation and not ignoring the fact that us developers still need to target Windows once in a while. That makes Fedora my favorite development environment by far.

But, alas, Linux drivers suck for laptops. I have a Dell and a port replicator at work and at home. I have a 24″ monitor at work running at 1900 wide and a 22″ monitor at home at 1680 wide. I swap between the two every day, and often work undocked at home with no external monitor. I could never get Linux to recognize when I dock and to figure out which monitor was hooked up. That drove me nuts.

A couple of things have also happened recently. I’ve been testing the Windows 7 RC on a separate partition and have started to really like it. As a lot of people have mentioned already, it’s what Vista should have been. It doesn’t quite have the flash of the Mac, but I find it’s a great balance between flash and the stability of XP.

The other thing that happened was that VirtualBox 3.0 has been released and it now has OpenGL support for both Windows and Linux guests. That was one of the reasons I moved to Linux, to experiment with OpenGL there. Now I can do that in a guest OS.

So putting all that together, I’ve replaces OSes yet again (been doing that regularly for years it seems). I’m now running on 64-bit Windows 7 with two major VMs, one for my fabulous Fedora dev environment, and one for the corporate XP environment I used to have there for Outlook and Netmeeting. So far so good. I get the odd glitch once in a while but nothing I can’t recover from and it is a release candidate. But now I have the best of all worlds. Except maybe MacOSX, and an iPhone dev environment. So close…


