---
layout: post
title: The JNI Debug Problem
date: '2009-08-25 21:04:00'
---


One thing I noticed the other day was that I’m doing a lot of JNI coding lately. In our Wind River Installer, based on p2 BTW, I have native code for doing a few things like compression and getting at the Windows registry. The CDT has native code for doing advanced process management, and getting at the Windows registry. I’ve played with Android native development which is all based on JNI. And I was thinking of hooking up the ALSA library to do Audio management with my prototype “Eclipse OS”. That’s a lot of Java/C coding. And, unfortunately, all without a debug solution :(.

JNI debugging was one of the early goals of the CDT. Unfortunately, it has never really materialized, at least not generically in a way we could incorporate into Eclipse. And given that I see a strong symbiotic relationship between Java and C/C++, I am getting more motivated to tackle this problem and see if we couldn’t come up with a solution that we can integrate into the JDT and CDT (or maybe just the CDT).

But the first thing you run into when looking at the code, where do you start? I’d like to be able to step into native methods, hit breakpoints in native code and see up the stack all the way into the Java stack. And really have an integrated debug experience where you don’t have to do much of a paradigm shift when going between the two worlds. And given the way the Debug platform is structured, that should be possible.

So there’s different ways to slice the cat (not that I slice cats, I like cats). You could add an extension point to be able to plug in native handling into the JDT debugger. I’m not sure what the JDT gang feel of that, or whether they’ve hopefully thought of that. Another solution would be to build a new Eclipse Java debugger component, but base it on CDT’s Debug Services Framework. That may make a more natural solution, but I fear it would be a lot of work and it would take a lot of investment to reach parity with JDT’s debug solution.

I’d like to hear what the community thinks. What is the right solution. Hopefully we can come together, find the development resources, and finally reach this Holy Grail for the CDT.


