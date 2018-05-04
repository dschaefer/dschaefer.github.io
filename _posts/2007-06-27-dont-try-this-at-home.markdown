---
layout: post
title: Don't try this at home
date: '2007-06-27 09:42:00'
---


I am putting the finishing touches on “CDT for Windows”, my self-contained CDT with MinGW distribution that I’ll be officially announcing later this week. To test it out, I thought I’d try it on my machines at home. One of them is this pretty old Pentium III 667 MHz (or as I like to call it in a throw back to my Iron Maiden days, 666 MHz, the processor of the beast, and I apologize if you’ve never heard of Iron Maiden 🙂 with 256 MB of RAM but with a healthy 80GB hard drive. We’ve been having real performance problems running anything other than a web browser on it, and even then, I can’t do things like TSN’s flash video clips. But, heck, I thought I’d give it a try anyway.

Whatever the minimal required machine for Eclipse is, this ain’t it. What a mess. It took forever to do anything. And all I did was create our Hello World project, build, and fire up the debugger. Now, I am using Apache’s Harmony JRE which is still pre-release, so maybe that’s not helping. But it’s amazing to see what memory starvation does on big software.

One thing I’ve heard off and on over the years is people complaining about the sluggishess of Eclipse and the CDT, especially on older Unix machines that had multiple users sharing resources. Now I see why. Luckily, developers using Eclipse usually have plenty of horse power and memory anyway and this isn’t as big an issue as it was a few years ago. But we still need to watch out. Even running the CDT on my 512MB, 1.8 GHz AMD Linux test machine at work has issues.


