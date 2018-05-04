---
layout: post
title: Android NDK Release 1 is Out
date: '2009-06-25 21:39:00'
---


I got a surprise today (aside from the passing of Michael Jackson), the Android Native Development Kit (NDK) team has [put out its first release](http://developer.android.com/sdk/ndk/1.5_r1/index.html). They never really hinted on their mailing list this was about to happen, nor did they actually provide a real time line. But it’s a good surprise.

The purpose of the NDK is to provide the ability to write native libraries that the Dalvik Java code can call through the Java Native Interface (JNI). This is the exact same interface we’re used to with desktop JNI so it’s quick to use. As I’ve mentioned here before, writing native code allows you to take advantage of the underlying hardware that Java hides from you. In this first release, it’s pretty basic, exposing only a few basic APIs such as the standard libc C run-time library, the math library, and libz for accessing compressed files. Just enough to accelerate some of your algorithms with direct execution by the CPU, which is ARM only right now.

There is still a lot missing, and they have promised there is more to come. OpenGL ES and audio are the big items on my wish list. At least I have enough information to be able to set up OpenGL ES so that it’ll run on my HTC Dream phone and the emulator. But there are no guarantees it will run on any of the upcoming phones since the ABI hasn’t been locked down. The GLES shared library name is the biggy (e.g. PowerVR as seen on the TI OMAP chips names their libs differently) although the header files should be the same.

The build system, though, has me very concerned. They’ve taken a lot of the concepts from the Android platform build system, which builds everything in one tree, and brought it to the NDK, including the restriction that everything has to be in one tree. I don’t build software like that. I put my native code in the same Eclipse project directory as the Java. I’m also working on a library that I want to use in a number of different platforms as mentioned in my previous entry. Android is just one target, it’s not the center of the universe.

I also noticed this when I took a look at Moblin. There is a standard way you setup a gcc cross-development environment. GCC has the facility to define a sysroot that organizes include files, and libraries in a natural way. And that allows for multi-target projects with very little change to your makefiles. Don’t assume you’re the only build system that wants to build my code.

One final nit, the Windows toolchain was built using Cygwin. Cygwin is a Linux emulation environment for Windows. As such it tries to hide as much of the Windows environment as it can, in particular when dealing with file paths. That messes up the CDT. We have some code that tries to deal with that, but the architecture is poor and we may loose that functionality over time. I’m a big fan of CodeSourcery and these guys are masters at building toolchains for multiple targets and run cleanly on Windows without Cygwin. Mind you, I’m pretty much solely on Linux now so that doesn’t matter to me as much any more. But others in the community will care.

Anyway, besides all that, it’s a great start. Native development and standard native APIs will be a key success factor for Android. We saw in the game console market how important it was for game developers to be able to target multiple platforms. That larger market allows for larger budgets which, of course, allows for better apps. The Apple guys get that and the iPhone SDK is very good, and at least for 3D Graphics and Audio, very standard. John Carmack of id (Doom and Quake) is a huge fan of theirs, but I wouldn’t mind seeing Doom titles running on my Android phone.


