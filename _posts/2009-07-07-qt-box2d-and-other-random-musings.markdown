---
layout: post
title: Qt, Box2D, and other random musings
date: '2009-07-07 12:01:00'
---


First of all, I’m very jealous of the Linux Desktop gang for holding their summit in the Canary Islands. I did a quick look at the cost and it’s not any more than what I spent to go to Stuttgart for Eclipse Summit Europe. I can’t wait to hear how it really was.

At that Summit, Nokia announced that they were moving from GTK to Qt for their Meamo Linux distribution for their handheld/tablet type devices. They were upfront about the reasons and it makes perfect sense. The plan is to have Qt as the default toolkit for Symbian devices as well. Learn one API and target them all. This is exactly what I hoped would happen with the Trolltech acquisition. So kudos to Nokia for a smart move.

And I hope through the Intel partnership with Nokia this will spread to Moblin too. For app developers, I think it’s really critical that we see some consolidation on the number of mobile Linux platforms. The nightmare I see supporting all the different Linux distros in my day job doesn’t need to be reproduced for mobile.

Anyway, that got me thinking again about Qt for my hobby activities. I want to learn what it takes to make games for mobile handsets and what kind of things the CDT would need to better support that. Having your work run on both mobile and in a simulation mode on the desktop makes a lot of sense, and one of the main drivers I see behind Windows adoption of the CDT. Qt would be a great framework for this for a few reasons. First you can target Windows and Linux desktop for simulation environments and the growing number of mobile platforms adopting Qt. And for me, Qt’s QGLWidget and Android’s GLSurfaceView work almost identically, further supporting my cross platform efforts. I’ll have to peak at the iPhone SDK and see if that holds true there too.

Speaking of gaming on mobile. Most of the games I see there are actually 2D games. There are probably a few reasons for that, but 2D games are just easier to do. There’s less pressure to actually simulate reality as you get with 3D. To help with 2D game development, a couple of guys in the Android community have ported the C++ Box2D physics engine to Androids NDK (Native Development Kit). Looking at all the cool 2D things I see on the iPhone and given the BSD nature of Box2D’s license, I can imagine its driving a lot of them. And the results are pretty cool, especially if you hook up the accelerometer on these platforms. I’ll have to play with it and see how easy it is to use.


