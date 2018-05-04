---
layout: post
title: How's build working for you?
date: '2008-08-06 15:34:00'
---


It’s been a crazy couple of months for me. The list of things I need to do has been badly encroaching on my time for Eclipse community work. But it’s all been good and we’re working on some really cool stuff with p2 internally here at Wind River which should turn into community work as well anyway.

But it’s getting time to start my work on e4 and the Eclipse resource model. We’ve talked a lot in the past about the need for flexibility there and to support other resource models that don’t necessarily map to the underlying file system. Even in the last few days we’ve received inquiries on the cdt-dev list about supporting Visual Studio-style projects in this manner (from a guy with an e-mail address of nvidia.com – quite interesting). So this is what we’ve meant by flexible resources and what we plan on addressing.

The question I’m starting to ask myself is whether we should be looking at the build side of the resource model as well. If you come from the Makefile centric view of the world, the Eclipse build system is very bizarre indeed. I’m not sure of the history of how it got to be that way, but it was our first real interaction with the Eclipse Platform team, to somehow get Eclipse to build CDT projects correctly. There’s still a lot of magic there that probably could be simplified if we made the build model more flexible as well.

Also we have a hell of a time co-ordinating loading the CDT build model data from our magic .cproject file at the right time and in a scalable and non-deadlockable way. Sometimes I just wish that the .project file and the code that manages it was more flexible as well so I can have our build data loaded at the same time the rest of the project information is loaded. (Yes you can do a little of that now but not easily with the complex data we have for our build configurations, tool chains, option settings, etc).

Anyway, I don’t know how many people are building IncrementalProjectBuilders out there (and, yes, the weirdness does start there). But I was wondering if other plug-in developers are also facing issues like this.


