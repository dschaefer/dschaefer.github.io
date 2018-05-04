---
layout: post
title: JDT/CDT, Can't we just get along?
date: '2006-09-26 15:11:00'
---


So between putting the finishing touches on CDT 3.1.1, some QNX work items, and dealing with the various summits and stuff, I’ve started working a little on my CDT/Windows Debugger API integration. It didn’t take too long before I got my workspace set up to work on it. I’m creating Java classes that will plug into the CDT’s debug engine (or engines as the new Debug Services Framework comes together). I’m also creating C++ code to implement native methods that talk to the Windows APIs. I’m also about to figure out the right way to do callbacks from those APIs trough my C++ code up into the Java code.

I’m trying to follow as much as I can the SWT model by doing as little in the native code as possible and putting most of the logic in Java. As much as I prefer C++ to Java, I don’t have a good answer to the question “How do you debug the debugger” so I’ll be relying on the Java debugger and good ol’ printfs to get me through.

But once you have a mix of CDT and JDT projects, the workflows aren’t pretty. The first thing that hit me was when I was in the C/C++ Perspective and hit the New Class button to create a Java class. Uh, nope, that creates a C++ class. So I’m starting to find myself flipping back and forth between the Java and C/C++ perspectives to get the right navigator views and toolbar buttons at the right time. It’s a pain and it would be nice if we had a “Code” perspective or something where we could write code without the context switching.

And then, there’s the result of my work. When I do get the debugger integrated, I may just wish to debug my debugger or some other JNI application with it. The “Holy Grail” for us in CDT-land has always been to be able to step from Java code into C++ code and back and forth seamlessly.

We’ve talked about this since the first CDT get-together back in July 2002. I’ve tried to get it to work with some success but got sidetracked with other things. The guys at Intel presented a proposal on such an environment at our Spring summit, bit I haven’t heard much about that since. I’m interested in hearing peoples’ opinion on whether this is something they feel is important for Eclipse. And, of course, I’m interested in ideas on how we can build a community to help make this happen. If nothing, it will be a lot of work.


