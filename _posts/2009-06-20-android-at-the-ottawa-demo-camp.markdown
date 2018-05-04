---
layout: post
title: Android at the Ottawa Demo Camp
date: '2009-06-20 13:17:00'
---


Well, my demo at Thursday night’s Ottawa Eclipse Demo Camp was a mitigated disaster. My laptop is in power hell as the batteries last only a few minutes and, of course, started to run out during the demo. The USB connection to may Android phone didn’t work and we theorized that laptop shut down the USB connections due to lack of power. So I couldn’t show that. I also ran out of time which I had a feeling would happen and I forgot to add a line of code that would have prevented the app from crashing.

Aside from that, I hopefully got my point across. Eclipse is a great IDE for doing Android development. The Java side is a natural and you get all the advantages of the JDT with the target management provided by the Android plug-ins. I also showed how easy it was to set up the CDT to write native methods in your Android apps. While not officially supported, there is an Android NDK (Native Development Kit) project that is under way to provide that support in an upcoming SDK release (donut I believe).

What I didn’t get to show was the two implementations of Android’s Kube demo, which shows a Rubik’s cube spinning around apparently trying to solve itself (being purely random, I’m sure it’ll solve itself just after the monkeys write that novel). It’s not a complex 3d object, with only around 3000 triangles (300 drawn 10 times per frame to give it some load), but the performance gained by writing the transformation matrix math in C++ versus Java brought the framerate from 25 frames per second to 36. That’s pretty significant. And on a mobile device where every CPU cycle drains a little bit of the battery, doing more with less is a key factor to a successful product.

At any rate, I had a great time that night. I got to catch up with some old buddies that I used to work at QNX with who are now doing a start-up just down the road from our Wind River offices. And there were some old buddies there from my ObjectTime days there as well. For some reason, these Eclipse events bring us all back together. It’s probably because Eclipse is huge in Ottawa. If your a tools developer here, there’s a pretty good chance your involved with it. And there are some pretty good tools developers here.


