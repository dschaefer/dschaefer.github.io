---
layout: post
title: What's next?
date: '2015-07-12 16:52:33'
tags:
- eclipse
---


The Eclipse Mars release marked a special moment for myself and our team at QNX and BlackBerry. It’s the culmination a few things we’ve really wanted to get done for our Momentics users and share with the greater Eclipse community.

It is focused around the Launch Bar and we’ve received great feedback from those who’ve tried it and those trying to adapt it for their own launch configurations and remote targets. And working with the community is why we do open source. We built it first for our BlackBerry Momentics users building BB10 apps and they loved it. But as we push forward we can learn and benefit from other IDEs trying to adapt it. It just makes the architecture better for everyone and ensures we can adapt it ourselves as we try to use it for new things. Open Source isn’t a charity so we give, but it’s also not a donation as we get a lot back in return.

Now that summer is in full force and I’ve finished off some vacation, it’s time to start planning for the next year. There’s still some work with the Launch Bar to do to clean up the rough edges and get it to the point where I would encourage all Eclipse packages to use it. I also want to continue the work we started with the PTP gang with the org.eclipse.remote target management system and make it a good replacement for the Remote System Explorer. I hope to get that in place by the Mars SR-1 release in September.

I also want to get back into improving Qt support in the CDT to make QML and qmake projects first class citizens so that the CDT is a good option to Qt Creator and let Qt developers take advantage of the Eclipse ecosystem.

That led me into the discussion about how to make it easier to add languages to Eclipse, in this case QML. There’s been some great discussion on the ide-dev list and other places with lots of ideas. I want to use ANTLR 4 for the QML work and am hoping I can generalize out of that so we can make it easier to add other complex languages like it. I’d like to extend CDT’s support to all languages supported by clang and LLVM. Even Swift if that’s the direction they take to open source it.

And it opens up an area in CDT that we really need to improve to allow us to take advantage of new toolchains and build systems. The CDT build system has always been somewhat cumbersome both for adopters trying to hook our tools up, and users who are trying to set up their build environments. We’re going to work with the CDT community to see if we can come up with a simpler architecture that takes advantage of the build systems, such as Qt’s qmake and CMake, that weren’t around or as mature when we started.

I also have my personal work on the Arduino C++ IDE for CDT. IoT is a great area of focus in open source and it’s really fun to architect an IDE for. You have a lot of choices in micro-controller (Arduino, ESP8266, and many upcoming Cortex-M* boards) and Raspberry Pi and other Cortex-A* boards. We really need to have CDT in shape for those developers.

But IoT goes beyond devices, you also have the cloud that they pass data to and get commands from, and then you have the Web and Mobile clients that hook up to the cloud. IMHO, Eclipse is the best choice as an IDE to build and debug all those components. And with my recent work at QNX, I have first hand experience at that and swear by it.

Lots to do and I’m certainly not going to get it all done when I want to, but we’ll keep plugging away and accept help when it’s offered and we’ll get there.


