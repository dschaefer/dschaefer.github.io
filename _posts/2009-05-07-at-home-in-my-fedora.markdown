---
layout: post
title: At home in my Fedora
date: '2009-05-07 15:07:00'
---


Well, it’s been about a month now and I’m starting to really feel at home with Fedora on my main machine, the Dell D830 laptop. The longer you go, the more packages you install that you find you need and eventually you end up with something pretty decent. My biggest issue was dealing with 32-bit apps and missing the 32-bit libs they need to run which you don’t get when your in 64-bit mode (I have 4GB RAM and want to use it all). But that’s pretty solvable if not time consuming. And then there’s the never ending issue of docking and undocking the laptop, going from single screen to my second 24″ LCD at work to my alternate second 22″ at home. I still have to reboot to get the thing to recognize the second screens, and I even get the occasional hang when coming out of standby. But I’m dealing with that.

There are some things that just rock. I’ve been playing with the VIA Artigo I got at ESC a couple of years ago and building embedded images and toolchains and kernels and libraries is a dream with the tools available on Linux. There’s no beating “-o loop” to peek at and create a file system image (just remember to type the right /dev name when doing a mkdosfs, doh!). Not to mention having all the utils and libs necessary to build cross compilers and such. And I’ve played with both buildroot and OpenEmbedded which are things you only want to do on Linux.

One thing I am learning though is that anything compute intensive probably shouldn’t be done on a laptop. I think I’m melting my video chip as the external screen goes into fits as the disk and CPU get busy. Not to mention the scorch marks on my legs trying to watch the NHL playoffs and build a cross gcc at the same time. So I’m starting to use my Dell desktop at work more where I’ve learned the slickness of “ssh -Y”. You can’t do that on Windows.

But I still have a Windows XP image running in VirtualBox for those times I do need Windows. I still use Outlook for work. There’s no beating it for the high volumes I get and the Calendar is top notch, and despite Evolution’s attempt at Exchange integration, it’s not quite ready for prime time. And of course, I need Windows to finish up Wascana 1.0 which almost ready for beta trials with Galileo. And I have a partition open to try it on Windows 7 (especially now that I mkdosfs’ed over my old Windows install, same doh!).

But I can’t remember how many times I’ve gone between the Windows VM and Linux and forgot which one I was in. That is telling me that the Linux desktop isn’t all that bad. I still hate the fonts (been complaining about that for years) and the multi-screen situation, but the rest is making it worth it. Highly recommended, at least if you’re someone like me.


