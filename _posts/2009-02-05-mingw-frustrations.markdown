---
layout: post
title: MinGW frustrations
date: '2009-02-05 12:36:00'
---


Um, yeah, Wascana 1.0 keeps slipping. Work has been very busy leaving little time for me to work on it, but that should be clearing up in the next few weeks (I hope!). But as I did my testing for the release candidate of CDT 5.0.2, as I expected, I ran headlong into the gdb 6.8 issue that everyone seems to run into. I don’t know how many people I see on my Feedjit log searching for: “gdb eclipse No source available for “ntdll!LdrAccessResource()”. And I hope those people now find this blog entry instead.

The issue is that before gdb 6.8, there was no way to issue pending breakpoints using the MI protocol we use to talk to gdb. I think it was introduced in 6.7 from the CLI, but that doesn’t help us. To support breakpoints in shared libraries, we need to keep retrying to set those breakpoints on every shared library load event. That worked for many years. But now, the break on shared library event in the MinGW gdb 6.8 really messes up the CDT. And it’s mainly because it doesn’t work in gdb any more.

So the solution is to add support for pending breakpoints, at least into the MinGW debugger target. But, alas, I think that’s going to be a lot of work. And given I’m having trouble finding time to even get the p2 support for Wascana done, let alone dive into debug which I don’t really have expertise on.

At any rate, the experience is so bad, I’m starting to think of holding off Wascana 1.0 until Galileo in June. I can make the p2 repo available so people can download the same thing I’m testing with. But until this debug issue is resolved, it’s not an environment I’m happy to send out to the world.

That and there was an interesting conversation on the mingw users mailing list recently about the state of gcc 4.x for MinGW. I’ve lost faith that it’s ready for prime time as well.

It’s enough to make me wish we had a Windows debugger available and to complete our Visual C++ support (wink, wink, nudge, nudge to people who know who they are ;). For now, [bear with me](http://answers.yahoo.com/question/index?qid=20060919122914AAof0Ad).


