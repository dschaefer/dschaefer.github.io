---
layout: post
title: TV's are small, plus a little Clutter
date: '2009-01-31 23:10:00'
---


So I was sitting watching my 40″ HDTV the other day, and started thinking about why web browsing on a TV pretty much sucks, even with all the pixels you get at 1080i or what have you. And trust me, I tried it with our PS3 and other than watching YouTube videos, it’s not a good experience.

But while I was sitting there on my couch (or sofa, depending on your English dialect) a pretty normal distance from the TV, I held my hands up to frame the size of the picture at arms length. Then lowering it to may lap, it struck me. The size of the picture isn’t any bigger than a handheld gaming box, maybe slightly bigger than an iPod Touch (as I try to find one for my son’s birthday on Thursday 🙁 ).

The reality of the situation is that even with the higher pixel count, you still need to treat set top boxes as mobile, but not mobile, internet devices and entertainment units. And that especially goes for the UI. Don’t try running GNOME on it, that’s going to be brutal.

So I’m off taking another look at mobile devices and the user interfaces they present. [The newest one is the 2.0 alpha release of Moblin](http://linuxdevices.com/news/NS2184863928.html), Intel’s effort at a Linux distro for mobile internet devices and netbooks running their chips. The video in the LinuxDevices.com article is intriguing, and made me go look at what technology they were using to present their 3D animated GUI.

Well, it turns out to be [another open source project called Clutter](http://www.clutter-project.org/). They produce a library that abstracts away the grunge of OpenGL and OpenGL ES to build user interfaces. You create Actors that have images and such and declare their animation and event handling and then fire off into an event/display loop. You get pretty cool effects with not too much code.

Now, I have to pick at the choice of GTK as their paradigm mentor and, yes, if you’re used to GTK programming, doing Clutter will be natural, but if you’re like me and fell in love with the Qt and it’s elegant use of C++, then you’ll be a little put off. I did find a clutter-qt integration in their repo, so maybe you’ll be able to do both in the future.

Someone once said, and I think he lived in Redmond, Washington, that there was no innovation in open source. This is a pretty significant counter to that. This project has been around for a while, sprouting out of the need to add GUIs on top of the new fancy 3D graphic chips appearing in handheld devices. They have a innovative and game changing solution. The just need people to discover them, and Intel, [who also happens to be their new boss](http://linuxdevices.com/news/NS7559902579.html), is helping with that.


