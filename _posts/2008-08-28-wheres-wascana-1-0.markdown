---
layout: post
title: Where's Wascana 1.0?
date: '2008-08-28 23:02:00'
---


For those who haven’t heard of Wascana, it’s a [lake in the center of my birthplace](http://www.wascanalake.com/), Regina, Saskatchewan, Canada. It’s a beautiful oasis in the middle of the bald Canadian prairies and my last trip there inspired me to name my [Eclipse CDT distribution for Windows desktop programming](http://wascana.sourceforge.net/) after it.

Around this time last year I realized that school was about to start and I rushed out the first release of Wascana 0.9.3. To date I’ve had almost 9,000 downloads of it showing me that there is interest and a need out there for such a package.

My plan was to get Wascana 1.0 ready for this school year. But my summer has been very busy and I haven’t had a chance to work on it. But hear me now and believe me later (I’m sure that was in an old Saturday Night Live sketch somewhere), it is still on my roadmap. For one thing, I really want to make it a showcase for the Eclipse p2 provisioning system showing how you can build a feature rich install and update environment for your whole IDE, not just the Eclipse bits.

Aside from that I want to add the boost C++ libraries to the package. Boost is a very full C++ template library that gives you a lot of the library functionality that makes Java so good, and it’s often a showcase for new technologies that end up in the C++ standard anyway.

I’m also waiting for an official release of gcc 4.3.1 for MinGW, to give us the latest and greatest compiler technology from GNU with super good optimization and support for OpenMP for parallel programming. There’s also the newest gdb debugger that gives pending breakpoint support so we can get rid of a lot of the kludges we had to put in place to support this kind of thing in the CDT. Unfortunately, Windows debugging for MSVC support isn’t as complete as I’d hoped, but there has been progress as part of the [Target Communication Framework (TCF)](http://wiki.eclipse.org/DSDP/TM/TCF_FAQ) work at Eclipse, so we will get there sooner or later.

And, of course, there’s Ganymede, including the latest CDT 5.0.1 which will be coming out with the Ganymede SR1 in a couple of weeks. CDT had some really awesome improvements, including new refactoring support, in the 5.0 stream.

So for those waiting, I’m glad your a patient bunch. The wait will be worth it for this critical piece of my continuing effort to get the grassroots C++ programmers and hobbyists, many of whom are working on Windows, into the Eclipse world.


