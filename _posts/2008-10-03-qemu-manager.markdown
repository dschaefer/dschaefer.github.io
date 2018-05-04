---
layout: post
title: QEMU Manager
date: '2008-10-03 21:32:00'
---


Shh, I’m supposed to be working, don’t tell my boss 😉

I wrote in a previous entry about the [VirtualBox SDK](http://www.virtualbox.org/wiki/Downloads), and the potential for using that SDK to add 3d graphics support. I was pretty excited. All I needed to do was create a DLL that could be loaded into the VirtualBox I used for running Linux on my Windows laptop. Well, I tried a simple example, but could never get the DLL to load. Looking at the source code for VirtualBox, I noticed that there’s a “hardened” mode for building it. For security, it prevents rogue DLLs from getting loaded. I guess my DLL looked pretty rogue :(. And [the complexity of building](http://www.virtualbox.org/wiki/Windows%20build%20instructions) VirtualBox myself scared me off.

I’ve also been a pretty big fan of the [Qemu emulator](http://bellard.org/qemu/), especially for emulating mobile devices. But you can use it for emulating a PC and there is an accelerator driver that apparently makes it fast. So I guess I could give that a try. I’ve mucked around in the qemu source in the past and I have an idea on how to add a device. It’s not as clean as the VirtualBox SDK promised, but it could be done.

Along the way, I found [Qemu Manager](http://www.davereyn.co.uk/download.htm), a nice GUI that manages virtual machines and launching them on Windows. Very cool. And it’s extensible so that if a new version, or a cleverly hacked version, of qemu comes out, you can have it manage launches for them as well.

So this weeks “Open Source Tools Kudos” go to David Reynolds for building the Qemu Manager. Very cool and thanks!


