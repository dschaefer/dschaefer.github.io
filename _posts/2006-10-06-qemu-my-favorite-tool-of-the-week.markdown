---
layout: post
title: Qemu, my favorite tool of the week
date: '2006-10-06 21:50:00'
---


I’ve been with QNX for over a year now and I continue to learn all I can about our Neutrino operating system, and development issues faced by embedded developers in general. If I’m going to focus on tools for embedded developers, I need to get inside their shoes and walk the talk.

I’ve worked with a couple of development boards and that was pretty cool, especially when lights started flashing and it started communicating out the serial and ethernet ports. But carrying around a board, even a little one, is a bit cumbersome and not very practical. I’ve been a long time fan of [VMware](http://www.vmware.com/) and have used that. But, x86 is not where the excitement is at in the mobile embedded market, so I have been looking for something that was less desktop-y to use.

Recently I ran accross an [article](http://www.aurel32.net/info/debian_arm_qemu.php) on using Qemu, an open source processor emulator that can emulate a number of different processors and peripheral devices, to run a Debian Linux ARM installation. It also claims that on faster machines, it can even be faster than the actual ARM processors it is emulating. This is exactly what I was looking for.

So I’ve started down a journey of writing a Neutrino BSP (Board Support Package) for Qemu, which emulates the [ARM Versatile Platform Baseboard](http://www.arm.com/miscPDFs/4989.pdf). I have the programmers guide for this board which is a pretty good help, but thanks to the fact that I have the source for the emulator, if I have any questions about how certain registers work, I can just look at the implementation in Qemu. The architecture is very clean so it makes these things very easy to find. It also includes a gdb remote interface that acts like a JTAG interface so I can step through my code.

With all these goodies, I think I’ll have Neutrino up and running in this environment in no time. Very cool! There is a [tutorial](http://cdtdoug.blogspot.com/2006/02/cool-eclipse-cdt-for-embedded-tutorial.html) floating around by James Lynch on using the CDT with a tiny ARM-based board. I should write a similar tutorial on using Qemu’s ARM emulation with the CDT and make sure these environments work well. It’s a great learning tool if nothing else.


