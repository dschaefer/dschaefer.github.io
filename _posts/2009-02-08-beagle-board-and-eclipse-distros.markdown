---
layout: post
title: Beagle Board and Eclipse Distros
date: '2009-02-08 20:49:00'
---


We had a meeting a few days ago amongst interested parties in an Eclipse IDE distribution for embedded. The idea would be to do something like I’m doing with Wascana which is supposed to make it easy for developers using open source tools, students especially, to get them up and running on Windows, and in turn showcase the features of the CDT in that environment. The idea of doing this for embedded would be to do the same for embedded systems developers and to show case the features of the DSDP project at Eclipse as well as CDT’s embedded development support.

One thing I think we noticed quite quickly is the diversity of the embedded community at Eclipse. We have Web services applications for embedded, we have J2ME Java for embedded, we have deeply embedded systems like microkernels and DSPs that have no OS per se, and, of course, we have the more traditional RTOS systems. I think it’ll be hard to showcase Eclipse support for all these things in one distro, and maybe it deserves it’s a few such distros, or maybe we have RTOS versus not RTOS. It’s an interesting initiative and I’m excited to see where it goes.

One of the platforms that came up in the meeting was the [Beagle Board](http://beagleboard.org/). Checking out their web site, it looks like an interesting target for hobbyist and student embedded developers. It’s a cheap little board at around $150 US (a little more once you add the needed cables and a power supply to use it properly). The community there is working on getting the Angstrom embedded Linux distro running on the board and there are some cool videos of it working. Don’t doubt it, this is being driven by Texas Instruments, who makes the chips for this board, so it’s not purely a community driven project, but it looks like an independent community has formed and is running with it.

I think this would be a good choice to target an Eclipse for Embedded distro. I think a case could be made for qemu as well and the various CPUs and boards it emulates. And I assume you’d target Linux for these platforms. But then you open up the questions, which distro do you support, or do you make your own? And what about the other free or quasi-free RTOSes that have Eclipse support. At a minimum you need a cross compile and debug tool chain to integrate Eclipse with but what else would you need?

I get the feeling that this could turn into a pretty big project on it’s own. Which, of course means it won’t happen without a community behind it and maybe vendors to sponsor it. I’m interested in hearing your opinions on what this all should mean and what you would like to see in an open source Eclipse for Embedded IDE.


