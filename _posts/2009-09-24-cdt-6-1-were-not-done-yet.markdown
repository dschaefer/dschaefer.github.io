---
layout: post
title: CDT 6.1, We're not done yet!
date: '2009-09-24 11:03:00'
---


We had a couple of really good planning sessions so far this September as we put our plans together for the next release of the CDT, CDT 6.1 for Helios. We’ve been focused on Build and Debug. We’ll continue to move the sticks forward for the editor and parser based features, but build and debug still have some major work to do.

On the build side, we’re focused on improving the CDT Scanner Discovery mechanism that scans build output to try and figure out the include paths and defines that you are using for your build. That information is fed to CDT’s parser to replicate the parse your compiler does. And that gives us pretty good accuracy to enable things like open declaration and content assist. This work will be a big challenge as we have a bit of a rag-tag group of part timers to try and get this problem area for CDT integrators and users fixed up. But it’s a great challenge for me as a project lead to see if we can get as much done as we can.

On the debug side, there’s some exciting news. As Ken Ryall from Nokia has been blogging lately, they’ve been working on a new debugger that’s much more tightly integrated with the CDT, and they’re ready to contribute it. Essentially, it’s a replacement for gdb. Now you can argue whether that’s a good thing or a bad thing, but I think it’s a good opportunity to improve CDT’s debug ability. And of course, it’ll be able to sit along side our gdb support which continues to be important for a number of vendors.

But part of Nokia’s work that has me most excited, is the native Windows debug support. This is an important step towards finally getting a complete Visual C++ integration for the CDT. I have a build integration almost ready to go. All that was left was debug support. While it is still missing support for Visual C++, Nokia’s Windows debug API support gets us maybe half of the way there.

The other good thing about Nokia’s work is support for gdbserver as the small agent that does the bit twiddling. Those who’ve done embedded development know about gdbserver as that’s how you do remote debugging of targets using gdb. Reusing gdbserver gives Nokia’s work a huge leg up for embedded developers working on all platforms that support gdbserver.

So despite being 7 years into our program, there is still work to be done on CDT. The community is still vibrant. We don’t have the big vendor contributions like we used to, other than Nokia of course, but there is still a lot of work to be done and individuals and smaller vendors who are interested in helping. So to quote Monty Python, we’re not dead yet :).


