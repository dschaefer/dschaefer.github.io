---
layout: post
title: We need a JNI helper plugin
date: '2010-04-28 09:37:00'
---


Now that I’m back being an engineer/architect, I’m again thinking of too many projects that I want to do with the time I have. I’m getting involved in the Target Communication Framework (TCF) which has an exciting opportunity to standardize target (in this case mainly embedded targets) communication and services for the purposes of debug and data collection amongst other things.

I am also trying to make it easier to use CDT for specific platforms. Windows and Android and soon Qt are the main ones there. But I’ve run into problems with the complexity of CDT’s build system that I need work with the community to clean up.

And there is another shiny object has caught my attention and I’d love to get time on that too. Our long term holy grail on the CDT has been to support developing native libraries for Java. The debug scenarios are scary, but I’ve been thinking of another area that should be a lot more attainable.

That’s automating the creation of the code that JNI development requires. There’s two paths. One is generating skeletal C code for Java native methods. And the other is generating wrapper Java classes for C++ classes. There used to be commercial products that did that, but I’m not sure if they’re still around. And given the power of the Java and C++ parsers we have in Eclipse, and the code generation frameworks available, it shouldn’t be that hard, you would think.

I think this would be a huge benefit to JNI developers, or at least me :). The interesting thing to note is that Android had the foresight to use JNI for their native interface so there’s a new community who could use it. If anyone is interested in doing something like this, give me or the cdt-dev list a ping.


