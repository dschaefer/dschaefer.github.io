---
layout: post
title: Hypervisors drive Heterogeneity
date: '2010-08-23 14:30:00'
---


<div></div><div>[![](http://1.bp.blogspot.com/_X6Gz24BqUwI/THLXrN1I00I/AAAAAAAAACU/rj0BmLOx1M0/s320/lab.jpg)](http://1.bp.blogspot.com/_X6Gz24BqUwI/THLXrN1I00I/AAAAAAAAACU/rj0BmLOx1M0/s1600/lab.jpg)</div>I have put together a pretty neat little lab here under my desk. As I always say, you have to use the tools to understand the needs of the users. You have to get into their shoes and see what you like and don’t like. Then you have a good chance of building tools they’ll actually use and like.

My lab includes two “embedded” systems on the right. The top is a board that has a Freescale PowerPC P4080 8-core chip in it. I have attached my Wind River ICE JTAG unit to it to test some really heavy duty multi-core scenarios. On the bottom right, I have what looks like a basic PC, and it is, but it runs Wind River’s hypervisor hosting three operating systems: Wind River Linux, vxWorks, and of all things Windows. I don’t have the P4080 system booted up yet, but my intention is to run the Hypervisor there too with random combinations of wrLinux and vxWorks.

As I put this together, it really drove home the need for an IDE platform that is heterogeneous. That’s a hard word to pronounce, but what I really mean is an IDE that can target any operating system that can run in a hypervisor configuration, which is pretty much all of them. And that means an IDE that has plug and play support that lets you create the source for applications that can run on them all, build that source for any and all of the target platforms, and debug the application as it runs on one ore more of them.

And, you guessed it, the Eclipse CDT C/C++ IDE is a great platform to do that with. We have build and debug support for the GNU toolchain for Linux and from Wind River we have commercial support for vxWorks and Wind River Linux, and upcoming in the next release of CDT, we’ll have support for Microsoft’s Windows SDK which includes Visual C++.

As well, I’m about to embark on a very interesting journey with the Target Communication Framework as we advance it’s debug capabilities to cover all of these platforms as well. With a common framework for agents that run in all these environments, we’ll have the ability to plug ‘n play capabilities into these agents and come up with tooling we haven’t even dared to consider before. Am I pumped about it? You betcha. We’ve long had the advantage of plug-in architectures with our Eclipse-based tooling, and now we’ll get that advantage all the way down to the target as well.

And it’s really these hypervisor scenarios that have brought me here. It’s finally a concrete example where you really need the heterogeneous capabilities that have driven my work on the CDT. And, it’s something to sell our employers with too :).


