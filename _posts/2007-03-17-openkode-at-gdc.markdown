---
layout: post
title: OpenKODE at GDC
date: '2007-03-17 11:36:00'
---


You know, all my dreams will have come true if I am ever standing at a conference center attending a GDC, the Game Developers Conference. Interesting enough, this year, it was held the same week as EclipseCon, and in the same area of the world, so I was close. But it is just a dream, and we can probably save that one for another life time. At any rate, I am always interested to see if there is any big news that comes from there, especially in the tools/SDK front that might be of interest to CDT users.

One thing I did notice was that [Khronos](http://www.khronos.org/), the open media API people gave a number of presentations there and have nicely [posted them to their site](http://www.khronos.org/library/detail/gdc_2007_handheld_technologies/). The one I was most interested in was on [OpenKODE](http://www.khronos.org/developers/library/gdc_2007/Handheld-Technologies/Handheld-Technologies_OpenKODE.pdf), a core API that allows you to build portable applications. What I found most interesting in that presentation was a “State of the Union” of handheld multimedia applications. It shows why the industry needs to be interested in standard APIs to allow for growth of applications for these devices. And I firmly believe that and am glad Khronos is taking this on. They also confirmed what I believe about Java, that, while it really helps with cross platform development, if you need performance, like most 3D applications do, you really need to code natively, and that means C.

In theory, with OpenKode, you can build for one platform, say Windows, and with a simple recompile, run your application on another, say a handheld device running some other operating system. This is similar in purpose to [SDL](http://www.libsdl.org/), but SDL has a patchwork architecture, where OpenKODE seems to be much cleaner. Acrodea has a [sample implementation](http://www.acrodea.co.jp/en/openkode/) of it for Windows, and I wouldn’t mind seeing someone do an open source licensed version of it so that we can pass it along in our upcoming EasyEclipse CDT distribution.

We can debate whether C code that requires a recompile to run on another platform is portable. However, if you look closely, to get any performance out of Java, you need a JIT which recompiles your Java anyway. With C, you just need to do it manually and ahead of time. As we build up a collection of portability libraries, I don’t see that there is a big need to jump on the Java bandwagon.


