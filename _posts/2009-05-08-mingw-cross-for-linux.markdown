---
layout: post
title: MinGW Cross for Linux
date: '2009-05-08 15:24:00'
---


I mentioned in my last entry that building stuff on my laptop leaves scorch marks on my legs (if you haven’t read it, that won’t make sense). This is especially true when building in my Windows VM. But I figure it wasn’t so bad when building from within Fedora itself. And since I knew from my experience on the MinGW mailing lists that the developers there mainly use Linux as their build hosts, I figured that maybe a better path towards building what I need for Wascana would be do it that way to. Build a cross-compiler that ran on Linux and built Windows libraries.

Then I remembered that I ran into Andrew Overholt from Red Hat and he was excited to let me know that they were working hard on mingw packages for Fedora. That was before my Fedora days so I kinda blew it off, as “sounds good, I guess” (sorry Andrew!). So when I googled to find out how to build a cross compiler for MinGW, of course, I ran into the work at Fedora that he was talking about. And it blew me away. Not only are they packaging up the cross compiler, they’re also packaging up a pretty thorough list of libraries to help you build Windows apps, many more than I was thinking of for Wascana.

So that’s led me to wonder, since I’m now a Fedora fanboy :P, why not sync Wascana up to these packages. That way, whether your building your apps from Linux or from Windows using Wascana, you have the same library set available to you. I should also make sure the versions line up for the toolchain so that there are no ABI issues on the C++ side (which probably isn’t a real problem anyway).

And interestingly enough, it brings into play the Cross GCC compiler integration that I build for the tutorial I gave at EclipseCon which I have just contributed to CDT 6.0. I should make sure you can use it easily in this environment too.

The team building the cross mingw stuff for Fedora have made all the decisions and I can extract what I need from their RPMs to install into Wascana. In fact a number of the packages already have zip files ready to grab with p2. Thank you Fedora team!


