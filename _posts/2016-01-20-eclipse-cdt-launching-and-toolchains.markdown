---
layout: post
title: Eclipse CDT Launching and Toolchains
date: '2016-01-20 13:52:06'
tags:
- eclipse
---


I’m working on adding debugging for CDT’s upgraded Qt projects support. Looking at the legacy CDT launch delegates, I’m having a hard time figuring out how to reuse the parts that I need. I’m not sure the old delegates have the structure we need to support the automated workflows we’re trying to do going forward.

Of course, this is driven by the work we’ve done with the Launch Bar. UI look and feel aside, people love the workflows it enables. You select the thing you want to launch, where you want to launch it and a mode for the launch and you hit play and it goes off and builds the thing and launches it without any additional interaction. Of course you can customize things but you don’t really have to if you just want to keep things simple.

I guess the problem we have next is implementing that. We’re essentially using launch configuration delegates for all this. I’ve added a sub-interface that adds the launch target, i.e. where you want to launch, to the methods of the delegates. And really, the buildForLaunch and launch methods are the only ones you really should be extending. The pre and final launch checks don’t have the ILaunch so I’m not sure how they’re supposed to check anything other than the configuration is valid.

The issue I run into next is that for a launch mode like Debug, I need to know what debugger makes sense for the given launch. Unfortunately in CDT, we’ve pretty much hard coded gdb everywhere so it’s hard to tell it to use a different debugger. But for Qt, I want to eventually support the Windows debugger cdb as well as lldb where available. What’s the best mechanism to do that without creating delegates for them which, trust me, if you have multiple delegates per config type and mode, you’re in for a world of UX hurt.

One thing I keep coming to as I look at renewing how we build and launch in CDT is that these two things are intrinsically tied. For whatever reason, we’ve tried to separate them but workflows are so much better if they know about each other. Builds produce the symbol files that the debugger needs at launch time. And usually the format of those symbol files tell you what debugger you can use. And for most SDKs out there, you get a debugger along with your compilers and linkers anyway.

I really thing the debugger needs to be a part of CDT’s concept of toolchain. The new CDT build system asks the build configuration, which knows what toolchain is being used, to do the build. We should just ask it to do launches too. Now that’s just a crazy idea.

Of course, I’m doing a brain dump here as I think about it. I may change my mind especially as I try and implement this. I’d sure like to hear other peoples thoughts and what other CDT extenders do. Most vendors who do extend CDT don’t usually use CDT’s launch configurations. I can see why since they’re both too flexible and inflexible at the same time. I just wonder if others have thought about this.


