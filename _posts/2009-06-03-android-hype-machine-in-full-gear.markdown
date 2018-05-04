---
layout: post
title: Android Hype Machine in Full Gear
date: '2009-06-03 19:54:00'
---


If you are following the news on Android lately you’ll wonder what the heck is going on. Soon, you’ll be seeing Android not only running on your smartphone and netbook and smartbook and netphone, but maybe your grandmother too. OK, maybe not your grandmother. But with Acer’s announcement that they are releasing an Android notebook in the third quarter this year, a real announcement, not just the rumours that we’ve been hearing for months now, Android is starting to spread it’s wings.

I really wonder, though, why that is. Why has Android turned into a hype machine as of late? Google expects 18 new phones out over the next year, and they gave everyone who attended the recent Google IO developers conference a free HTC Magic developer phone (wish I was there 🙁 ). The timing of all these announcements shows me that Google really has a pretty active marketing department, even if they seem to be behind the scenes, and even as the face of Google always seems to be their engineers.

Anyway, if you’re writing an Android app, check the screen size on start up and change the layouts accordingly to support all these form factors. And if you’re writing native code, get ready to recompile for x86 as well as ARM. Oh, and apparently MIPS is now in the mix thanks to RMI and Embedded Alley. I’m not sure whether the hype will continue to grow and whether the consumer excitement will match, but it’ll be interesting to watch.

BTW, I always wondered why vendors list Android and Linux, isn’t Android a version of Linux? Well, actually no it isn’t. Sure the kernel and the drivers are based on the Linux kernel and drivers. But user mode is very different, and for a reason we at Eclipse are quite used to. The Android team is avoiding GPL and LGPL like the plague. It makes sense as it allows for vendors to make custom versions of the libraries as they see the need. But it’s been a yeoman’s effort to make sure all the good things you get from regular Linux are available in Android. It does take a little time to get used to, at least if you’re playing with native libraries, and it is a good showcase for the CDT to show how flexible it is supporting new platforms.


