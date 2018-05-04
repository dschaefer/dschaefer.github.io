---
layout: post
title: MinGW gcc 4.3 - not quite dead yet?
date: '2008-02-11 16:30:00'
---


As I march into the exciting world of Virtual Instruments and VST and using the CDT build something I think is really cool, I keep running into the question: what toolchain should I be using for Windows development. Without a debugger, what’s the point of using the Visual C++ compiler. My gut tells me that it’s probably got a better optimizer than the old 3.4 that MinGW has at the moment, and that will be key to building a high performance plug-in for digital audio workstations.

At the [end of a recent blog entry](http://cdtdoug.blogspot.com/2008/02/yearning-for-good-windows-toolchain.html) I whined about the lack of progress with MinGW. On reflection, I really need to stick with my guns. As a lead for an open source project you know the first thing I would do with someone complaining something like that is to ask them where their contribution was. So I turned it around. How can I help MinGW move up to the latest gcc and gdb and get it all working nicely?

I kept hearing that the gcc had listed mingw as a secondary platform for the upcoming gcc 4.3, yet in the changelog and gcc mailing list, I haven’t really seen much progress. But maybe I’m just looking in the wrong places. So I set out to see if I can build it and run some tests. Building gcc is not for the meek and requires the exact right build environment. I was actually able to build it with a simple configure and got a C++ hello world to work. Very cool, and a great sign that someone out there in gcc-land is taking mingw seriously.

So searching around for instructions on how to build the gcc libraries (libgcc and libstdc++) as DLLs, I ran across the mingw-users mailing list (duh, why hadn’t I singed up for that list before?). It appears that there is progress being made in this area. I was kindly provided with build instructions from the former gcc guru on mingw who appears to be taking a closer look again. So I’m going to try to reproduce the build and help him out. If we can get another couple of guys doing the same thing and providing patches where things are broken, we should be able to get this into release shape.

In my mind that would be huge. With gcc 4.3 with it’s strong optimizer along with other goodies like OpenMP, we’ll have a great compiler for Windows development and for [Wascana](http://wascana.sourceforge.net/). And then I can focus on gdb, which also appears to be making progress at mingw. Things might not be as stark as I had made things out to be, especially if I put some effort in helping out.


