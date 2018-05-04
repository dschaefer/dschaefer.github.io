---
layout: post
title: My take on Android Keynote at Google I/O
date: '2010-05-20 20:04:00'
---


No, I’m not at Google I/O, despite my twitter traffic during today’s keynote. Mind you that was probably a give away that I wasn’t there as even the Googlers struggled with wifi connectivity during their demos. At any rate, I was glued to see where Google was taking Android. And, to be honest, they didn’t really surprise me much as pretty much everything they announced had a rumor associated with it. It’s hard to keep secrets in this industry.

Despite the lack of surprises, there were a few interesting points that were made, and a couple that were not which gave me pause.

First, was Google TV. Yes it too was rumored and came out pretty much as was rumored. There were two things I found interesting about it. And no, a set top box based on Android isn’t one of them as we pretty much expected that eventually. No, first was confirmation that the initial Google TV boxes will be based on Intel Atom chips. What that means is the real first confirmation of an x86 port of Android from Google officials. The new Android Native Development kit r4 that also came out today also confirms it with an x86 port of the native libraries. It’s not quite cooked yet as there’s no toolchain to build with and no image to run on, but they’re there and a sign of things to come.

I guess the other thing that struck me about Google TV that I think was even more interesting was that they were running Google Chrome on top of Android on top of x86. I’ve heard rumbling about the lack of information about Chrome OS at the conference. Now, if they have Chrome running on Android for Google TV, why not run it on netbooks too? And then why have Chrome OS at all. That’s where I’m guessing there won’t be one or if it does appear, we’ll all be wondering why when you can get all that plus Android apps to boot just like on Google TV. Or, maybe, that is what Chrome OS is. We’ll see (or maybe not)…

So there were a few new things in the Android NDK for me to chew on. One that will make the CDT build integration I’ve been working on easier to do is the ability to build outside of the NDK directory tree (weird, yeah, but they previously reused the build system from the platform that is done that way). So look for that sometime in the near future. There’s also gdb support for native applications. I’ll need to see what’s needed to hook that up to CDT’s debug interfaces. In the end it’ll be a great public example of how to use the CDT in a cross compile and remote debug scenario. Not to mention it’ll be fun to use :).


