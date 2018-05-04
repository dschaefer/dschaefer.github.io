---
layout: post
title: Eclipse on Android, or Android-like usability for Linux?
date: '2011-04-21 21:58:00'
---


If you follow my blogs and my [tweets](http://twitter.com/dougschaefer), you know me as an Android fan boy. There are a number of reasons why but the main ones are that it provides a huge leap in usability and I can build from source myself and get it running on any device I want. And that includes x86 PCs, some provided by [AOSP](http://source.android.com/source/building.html) itself and a lot from the valiant effort put on by the [android-x86](http://www.android-x86.org/) gang. And now having seen live action [videos of the ASUS Eee Pad Transformer](http://www.youtube.com/watch?v=FEQqXi-3NpU), the Android tablet that transforms into a netbook, I am even more convinced how cool it would be to have Android as my PC environment.

But, there’s a problem. The applications I use, and that of course includes Eclipse, don’t run on Android. I also spend a lot of time doing embedded system platform builds and the Android user-space is missing almost every utility I would need, including the gnu compilers. Now nothing technical prevents these things from being ported over to Android as it is built on a Linux/FreeBSD inspired base and you could probably work around the few twists that come with it. And I do know a few people that would love to see Eclipse running on these Android netbook type devices. And maybe there is a future in that.

On the other hand, I have everything I want on Linux. But I find the usability horrible. I’ve had a chance to play with GNOME 3 with Fedora 15 and it is a big improvement, but I fear we’ll be living a long time with the legacy GTK-based tools which are really getting out-dated. Even Qt comes with it’s own set of issues.

I blame it all on X in the end. It probably doesn’t deserve it, but I’ve been an X user ever since I built X11R2 myself 20+ years ago. It’s old and it’s done. The new effort behind the [Wayland](http://wayland.freedesktop.org/) display server provides a much better architecture IMHO. It gets rid of all the X legacy and builds directly on top of EGL and OpenGL ES. That should give us the flexibility to do some really good things with usability with the help of accelerated graphics hardware and physics engines. That’s what Android Honeycomb does, and there’s no reason why we couldn’t provide an equivalent environment for Linux. It’s just a matter of someone driving the vision in that direction.

And who knows. Once Wayland is in place, how much effort would it be to provide the Android run-time mixed in with the Linux user-space. The RIM guys have figured that out with the PlayBook and their Android support someone astutely coined FrankenBerry. Wayland could easily support a client that drew at the command of an Android app.

No matter how you slice it, it’s a great time to be in the software business. The mobile guys are driving innovation in usability. Us desktop guys need to find a way to catch up.


