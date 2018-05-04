---
layout: post
title: An ARM on Family Day
date: '2009-02-16 15:09:00'
---


It’s “Family Day” here in Ontario, Canada, and while my one son is over at his buddy’s house and my other son is watching game trailers and my wife is out for lunch with the girls, I’m sitting here enjoying the day off. I’m sure we’ll do something family-ish later today…

Anyway, I just read about [TI’s new family of chips, the OMAP4](http://www.linuxdevices.com/news/NS9955815446.html). The big news is that this is the first time TI has jumped on ARM’s multi-core bandwagon and the mixture of parts going into these SOCs is quite impressive. You have PowerVR’s venerable SXG OpenGL ES 2.0 engine, image processing, and enough power to play 1080p video. As the TI guys says in the LinuxDevices.com article, this type of architecture really will start to blur the lines between smartphones and MIDs (and even makes me wonder about the set-top box market). It looks like we’ll be seeing some pretty exciting products ahead.

Speaking of TI, I’m still looking at the [BeagleBoard](http://www.beagleboard.org/) community-based development board kinda thing. The more I look into what the community is doing with it, I really see it’s potential as a vehicle for learning embedded development. But I’m cheap, so my attention turned towards whether the qemu emulator could emulate the BeagleBoard so I can run it on my laptop. And apparently [someone is working on it](http://beagleboard.org/project/qemu-omap3/). But then I started doing the math. How much is my time worth? Versus forking out the $300 or so to get set up. Makes me think…

Mucking around with all this has led me back to my [EclipseCon tutorial](http://www.eclipsecon.org/2009/sessions?id=248) on integrating a cross-compiler toolchain for the CDT. I really want to show how easy it is to get up and running with qemu and a cross-compiler and the freely available embedded Linux run-time goodies all under the CDT as the IDE. And given all the hype about ARM and mobile, I think I’ll go with ARM as the target CPU. Should be a fun 4 hours, which should be plenty of time to get at least a hello world running. I can’t wait and I really hope you can make it too.


