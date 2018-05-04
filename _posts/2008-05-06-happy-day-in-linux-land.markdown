---
layout: post
title: Happy Day in Linux-land
date: '2008-05-06 20:09:00'
---


Thanks to everyone for their great comments on [yesterday’s entry](http://cdtdoug.blogspot.com/2008/05/frustrating-day-in-linux-land.html) on the frustrations I had getting ClearCase running on my new Linux machine. It gave me renewed hope that I could get this to work.

And I did. After reinstalling Fedora 8 as the host OS, I started getting a KVM virtual machine ready. I figured I’d try the new Virtual Machine Manager GUI to do it just like I do with [VirtualBox](http://www.virtualbox.org/). But when they say it’s not ready for prime time, believe them. They’re on the right track but to do anything serious, I think you still need to use the command line.

Another hurdle I ran into was running the 32-bit version of RHEL. I guess I should have looked harder at the KVM web page that said SMP was unstable in this configuration. It was. So jumping to the 64-bit version, I was good to go, 4 CPUs and a bridged network connection and all! I installed ClearCase and I’m in business. Now it’s time to get some real work done. It was fun and I did learn a lot and gained an appreciation for virtualization, so it was well worth it.


