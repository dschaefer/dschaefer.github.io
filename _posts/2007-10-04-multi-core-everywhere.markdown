---
layout: post
title: Multi-core everywhere
date: '2007-10-04 13:30:00'
---


I was just reading about ARM’s [latest announcement](http://www.arm.com/news/18688.html) for their new A9 processor core. I’m a bit of a fan of ARM and not just because they have a committer on the CDT :). They have a very interesting strategy when it comes to their market and rely fairly heavily on open source tools to enable software developers to use their small low power cores.

What struck me about the A9 core is that it comes with built-in support for multi-core configurations of up to four cores on a single System-on-Chip (SOC). One of the concerns I have heard of ARM in the past is the performance of their cores, particularly their earlier versions. Going multi-core makes a lot of sense to help alleviate that without too much of a power overhead. And it opens up a new class of software application that can take advantage of it.

But once again, the spectre of doing multi-threaded development is starting to take hold in another sector of the industry. Are embedded tools ready to handle this? Even more important, are embedded developers ready to handle it. This is a recurring theme in my blogs and I still haven’t found the answer.

My gut tells me the best way for programmers to deal with the complexity of multi-threaded development is to introduce a new programming paradigm that simplifies the thought process and puts doing multiple things at the same time as a first class citizen. This is what we did when programs became gigantic and the old functional approach didn’t scale. Objects were our saviour.

The era of multi-core brings new challenges and I wonder out loud, is there a better paradigm to help us deal take advantage of all power it brings while allowing C and C++ developers to leverage their skills at embedded development? Is OpenMP the answer? Or does it go far enough as a new paradigm? Something to look into.


