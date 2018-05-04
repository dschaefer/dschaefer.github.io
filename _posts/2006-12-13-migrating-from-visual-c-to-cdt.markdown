---
layout: post
title: Migrating from Visual C++ to CDT
date: '2006-12-13 13:18:00'
---


I’ve put the finishing touches on the CDT’s managed build support for the Windows SDK. Well, at least there’s enough there for people to try with our upcoming CDT 4.0 milestone (M4, but it’s really our first for this release). It auto-detects where you’ve installed the compilers, header files, libraries, etc., by looking it up in the registry. I’ve also updated the error parsers to more accurately parse compile and link errors. It works pretty good and I’m using it to build the native code for the Windows debugger integration.

But, you know, I forgot about the standard builder. It’s funny how you get tied up in solving the hard problems when the easy ones are there staring you in the face. I have to give a big thanks to three guys from IBM India who have [written a tutorial](http://www-128.ibm.com/developerworks/library/os-ecl-vscdt/index.html) on how to import Visual C++ projects into the CDT. The solution is elegant in its simplicity and really shows the flexibility of CDT’s standard make projects.

All you need to do is get Visual Studio to generate the makefile for you. This is a feature that they’ve always had to support external builds (although in recent versions you can run Visual Studio headless to do builds as well). Then you create a CDT project at the root directory containing your source. Of course you’ll have to change the make command to use nmake, Microsoft’s own nasty version of make, but that’s pretty easy to do and works well.

Combine that with [this guy’s](http://clintonforbes.blogspot.com/2006/12/100-features-microsoft-should-steal.html) perception that the CDT has certain features that Visual Studio users would like, and the discussions I’ve had with embedded developers using CDT but using Visual Studio for emulation on Windows, gives me a warm fuzzy that supporting the Windows SDK is the right thing for the CDT. There are Windows developers who are looking for a migration path to get into the Eclipse ecosystem.


