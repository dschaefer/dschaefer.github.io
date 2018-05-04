---
layout: post
title: Yearning for a good Windows toolchain
date: '2008-02-03 23:10:00'
---


I’ve really started to get into this software synthesizer thing with [VST](http://en.wikipedia.org/wiki/Virtual_Studio_Technology) albeit the older 2.4 version since most digital audio workstations don’t support the new one (they could learn a lesson from Eclipse about keeping a community happy with API stability). There is a pretty good community sharing ideas and tips and examples. And it’s a pretty low overhead activity that has a better chance of turning into a hobby than some of my other grand schemes. Most free software synths seem to be build by individuals (versus my desire to explore game development – ever see the credits at the end of a game?).

So I’ve started with the basic VST headers and threw away their SDK since my ego says I can do better (just kidding :). I’ve got enough so that I have a synthesizer that produces silence. ZeroMemory() is your friend. I’m using the CDT, of course, with the Microsoft Visual C++ build integration I’m working on. It builds fine once I figured out how to get DLL export files (.def) so that the right symbol gets exported. In a bizarre twist, they look for a function called main with a different signature than the usual C main, which causes a compile error with the MSVC compiler.

At any rate the biggest stumbling block I ran into was the lack of a CDT debug integration for Windows. I’ve had to resort to sprintf and popping up MessageBox dialogs to see if code gets hit and to show values. That’s fine for simple things, but I found myself missing a real debugger integration as I’ve started to get interested in the more complex data structures I need to deal with.

Maybe working on a Windows debugger would make a good Google SOC project. And any student looking for ideas, feel free to make a proposal. Ideally, with all the talent working on gcc and gdb, I’d love to see gcc 4.x for MinGW and I’d love to see (or maybe I just need to figure out) how gdb can be used to debug gcc created DLLs with MSVC created applications. But I find it really disappointing that there isn’t a bigger community working on better gnu tools for Windows development.


