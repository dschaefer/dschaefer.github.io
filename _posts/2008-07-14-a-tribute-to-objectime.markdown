---
layout: post
title: A tribute to ObjecTime
date: '2008-07-14 22:12:00'
---


[As I mentioned recently](http://cdtdoug.blogspot.com/2008/07/lesson-on-systemc.html), I’ve been thinking of how you could program UML-like actions using C++ in a manner similar to SystemC. As I worked through the workflows of how actions could receive data and signals on input pins and send stuff on output pins, and how they all hook up together, I started to get a deja-vu feeling.

It brought back a lot of good memories from my years at [ObjecTime](http://en.wikipedia.org/wiki/ObjecTime). You know, we had a lot of this stuff back in the 90’s. Mind you, it was almost totally focused on state machines that communicated with eachother using messages, but it had a lot of the multi-threading, action oriented development that we need for multi-core systems.

It was a fun time back then. We were a company of 150 or so working on something we were all very passionate about. It was one hell of a team. And we had some big customers but not many of them. When Rational bought us we saw it as a good thing that would lead our work to greater exposure and a bigger sales force. It didn’t pan out that way, but the team lived on and a lot of them are still working on modeling tools for Rational which is now a division of IBM.

But one area where I think we failed was in adoptability. We had some passionate early adopters as customers but there are only so many of those. You certainly don’t want to build a business with only that. And it was hard to get the code centric guy to trust the modeling and code generation tools. Let’s face it, when it comes to crunch time, you’d rather be in with the code with age old and trusted tools and the modeling tools easily fall by the wayside.

Anyway, that’s why I work on the CDT now. Code rules, at least for now. But as we try to introduce complex programming paradigms to facilitate multi-threaded development, I got to wonder if there isn’t another ObjecTime out there. We where years ahead of the industry and we knew it. I had feared that the time would never come, but maybe that’s not true after all.


