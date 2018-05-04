---
layout: post
title: Using Eclipse CDT with MSYS2
date: '2016-11-08 14:46:36'
tags:
- eclipse
---


MSYS2 is a relatively new distribution to support the MinGW compiler on Windows. It’s actually grown beyond that and has a pretty rich set of packages that include CMake, clang and gcc, and a huge set of libraries including Qt and SDL. It’s kept reasonably up-to-date and I’m sure if we can grow the community even more, we could get things even faster (e.g. Qt is one minor release behind).

On Windows, the CDT loves MinGW and MSYS. As Eclipse is a native application, it really expects things like path names and such to be native Windows things. Cygwin, being a Linux emulation layer, and the recent Bash for Windows are actually hard for CDT to integrate with because they hide away the native.

For Eclipse Neon, CDT has added support for automatically detecting the MinGW compilers in an MSYS2 installation. This article will give a quick guide on how to set up MSYS2 with the proper set of packages to start building C++ projects on Windows.

First a quick rant about their choice of package manager, pacman. I’m sure people who use Arch Linux love pacman. It’s pretty powerful. But I worry that it’s a tough fit for Windows users. The problem gets worse as there are actually three sets of packages, msys (common), mingw32 (for 32-bit tools), and mingw64 (for 64-bit tools) and some packages are in multiple of those. pacman makes you pick each time you install a package. And it gets worse installing the toolchain since mingw32 and mingw64 each have toolchains that target 32-bit and 64-bit. Now you’re up to five combinations.

But it’s what we got so we’ll have to make due. Hopefully we can simplify this a bit.

First, most people are on 64-bit Windows these days and for that, just select the mingw64 packages and the x86_64 toolchains. If you are on 32-bit Windows, go mingw32 and i686 toolchain. If you are targeting both 32 and 64 bit, simply add the other toolchain. But also make sure you add all the libraries for that architecture too.

MSYS2 starts with a pretty decent installer. It’s available from [https://msys2.github.io/](https://msys2.github.io/). The instructions on that page are a good description on how to do the initial setup. After finishing that, you still have no toolchains or libraries. To set up your development environment, run the following command. This gives you gcc and make, enough to build a hello world project.

pacman -S make mingw64/mingw-w64-x86_64-gcc

A couple of quick notes on that. The toolchain comes from the mingw-w64 project which produces both 32-bit and 64-bit compilers. Confusing? Yes. Also, pick the make from the default package set since it’s a more full featured make than the mingw32-make that comes with the mingw64 package set.

That should be enough to get started. Feel free to poke around and add library packages you’d like to use. Qt projects should just work with CDT’s new (and still very young) Qt plug-ins.

More later as we figure out the right configuration for CMake and for other libraries.


