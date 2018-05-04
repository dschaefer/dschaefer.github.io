---
layout: post
title: Understanding C/C++ Build Systems
date: '2010-02-22 14:53:00'
---


My main development task on the CDT these days, when I get to tear myself away from other interesting things I’m looking at, is on a prototype of my dream CDT build system. I was involved in CDT’s managed build at the very beginning but let others run with it as I concentrated on the CDT’s source navigation features, parsers, and indexer. Now that those things are in really good shape and debug has a lot of good people working on it, I thought I’d take another look at build.

*(BTW, I’m back working mainly on Eclipse open source these days after two fun years of working on commercial p2-based installer technologies)*

Probably the biggest change over the 5 years since my first foray into build is that there are a lot of managed build systems out there now. Everyone seems to agree that writing Makefiles is hard but that there are patterns that can be deduced and can be codified in Makefile generators.

One of the earliest examples of that was the autotools used on most gnu projects. These tools generate configure scripts which then generate Makefiles and header files for given run-time configurations. The guys at Red Hat have a pretty good integration for autotools with CDT projects as a part of the Linux Tools project. But I know Jeff had a hard time putting the integration together and I hope to make that much easier.

There are others out there as well. CMake is very much like autotools, but a little more general and less gnu specific. It can be used to generate Makefiles for Microsoft’s nmake and Visual C++ for example. There is an Eclipse editor for the CMake input files but it would be nice to be able to cleanly integrate it into CDT’s build system.

Probably the biggest one on my radar is Qt’s qmake Makefile generator. It’s specific to Qt’s structure, but does a great job of managing the build system for Qt projects. As Qt becomes more popular, especially in the device community with Maemo and now Meego along with Symbian and Qt’s desktop offerings, it’s important that we provide good support for it.

Along with CDT’s existing build support for user provides builds (good ol’ Standard Build), and CDT’s Visual Studio-like managed build which has both a Makefile generator and an internal implementation of something like make, I think we need to be open to different types of build systems for the CDT. This is especially true for existing commercial products that have their own build systems created for their own specific needs.

It’s my firm belief that the growth of the CDT, including into the commercial space, requires that the CDT be as similar as possible across all these different instantiations of it, both open and free and commercial. That way users can leverage what they learn from one instance and apply it to the next. Build has gone in many different directions, but I hope to try and bring at least a little unity to what is otherwise a bit of a mess.


