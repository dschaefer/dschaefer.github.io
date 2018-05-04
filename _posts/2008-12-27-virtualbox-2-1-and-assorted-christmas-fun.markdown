---
layout: post
title: VirtualBox 2.1 and assorted Christmas Fun
date: '2008-12-27 13:45:00'
---


Just some random thoughts on this Saturday after Christmas. My family and I had a good Christmas, despite a little “Fun with Autism” moment with my Autistic son, but it’s all better now (patience is a key survival technique in our household). Yesterday was Boxing Day in Canada, which is a holiday here despite all the stores being open for your shopping pleasure. If you don’t feel like going out, you are free to sit around, well, like boxes, which we did for the most part.

I’m spending a little time today while everyone is playing on the PS3 and various PCs around the house getting ready for my [EclipseCon tutorial](http://www.eclipsecon.org/2009/sessions?id=248). I’m really looking forward to it. By the end of the tutorial, you’ll walk away with Wascana which you use to build qemu, a little Debian Linux image running in that qemu, and a cross-compile toolchain and CDT integration that you also get to build to create apps for Debian from Windows (and maybe Linux). Lots of hands on and hopefully an appreciate of why the CDT is the first class cross-platform C/C++ development environment.

Before I get back into playing with qemu, it was cool to see a [new version of the VirtualBox](http://www.virtualbox.org/) emulator come out, 2.1. It’s a minor version increase but there are two significant features added. One, is 64-bit support on 32-bit platforms. This is critical for me and my installer work at Wind River, where I need to test and debug on 32-bit and 64-bit platforms. I don’t trust 64-bit Linux enough yet to make it my main Linux environment, not to mention downright fear of 64-bit Windows.

The other cool thing is more on my personal interest front. They have an initial release of OpenGL support. If you read this blog regularly, you’ll know I have a dream of an open Linux-based game console/multimedia set top box. I’d like to try some ideas out on a Linux platform with 3D hardware without actually buying any and this is the first emulator to have OpenGL support.

Unfortunately, they only have Windows guest drivers at the moment but have promised Linux/X drivers soon. I can’t wait, but it does lead me to drop my plans for working on OpenGL support for qemu. Instead, I really need to spend what little hobby time I have learning how to write an X window manager, using a cross-compile environment with the CDT, of course 😉


