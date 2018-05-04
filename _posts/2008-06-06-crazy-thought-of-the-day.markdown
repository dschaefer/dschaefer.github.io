---
layout: post
title: Crazy thought of the day
date: '2008-06-06 15:07:00'
---


It’s Friday. It’s been a pretty busy and long week. Got lots done. Working on lots of Eclipse related projects both internal and external. The Red Wings won the Stanley Cup (although I’m very proud of the Pittsburgh fans for their behavior after their team lost at home, they’re real hockey fans). I bought a new car (a little Mazda 3 Sport, love it! but hate car shopping). So I think I’m allowed to think some crazy thoughts once in a while.

This one sprouts from a couple of different triggers. First, the latest Emacs discussion and how it would be nicer if we could integrate Eclipse better in a command-line environment. Second, comes from my interest in GUIs for embedded systems. Flash is one idea and trying to figure out how you’d hook a C/C++ app on a device to a Flash-based UI. Third comes from a bit of OSGi envy in that it would be a huge help to C/C++ developers if we had a component system like it.

So the crazy idea is this. Rewrite Eclipse in C++. Maybe rewrite isn’t the right word since I hear there are people out there who actually like Java ;). But start producing C++ components that look a lot like Eclipse. I’d start with SWT which is a layer over top of some C and C++ code anyway. Shouldn’t be that hard. You could then look at a C++ implementation of OSGi. Bundles would be easy to make, just use DLL/so’s instead of jars (of course, I’m missing the point on other componentization issues that OSGi deals with but I can’t be that far off). Then continue to add things as they make sense or people have a need.

I did a quick search, since I’m pretty sure the C++ SWT idea had been thought of before. I found a company, [PureNative Software](http://www.pure-native.com/), that has actually done it. Mind you, they are using their proprietary Java to C++ compiler to do it, and I would think that leaves in a lot of the glue that SWT uses to bridge the Java/C++ world. But they do have a compelling story.

So I’m going to try and contact myself in a parallel universe to start working on it. Or maybe it’ll just remain a dream. But I’ll throw it out there to see whether you think it’s such a crazy idea or not.


