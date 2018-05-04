---
layout: post
title: Android Notes and Ideas for Eclipse
date: '2009-10-05 17:58:00'
---


Here’s a few notes on things I’ve been doing with Android. I’m under no delusion that I can actually create an app for Android. My wife wouldn’t be too happy if I spend the time it would need. But I am finding that this is a great exercise getting into the mind of a mobile developer and is giving me ideas on how to improve the CDT and the Eclipse platform.

I’ve been working towards constructing a game engine, something I’ve always dreamed of doing. I am starting with the physics/collision detection engine and looking to open source for solutions. I started with box2d and wrote a little demo that had 20 “marbles” (ok they look more like squares, but squares are easier to render with OpenGL 🙂 that rolled around the screen as you tilted the phone. Essentially, I configured it to alter the gravity of the “world” to match the orientation of the phone. It’s a neat demo and gave me a hint at how to use engine and how much horsepower it needed.

But in the long term, I’d like to support the 3rd dimension (love the Simpsons episode when Homer fell into the 3rd dimension :). There’s another open source engine called bullet that does it. Interestingly it’s very similar to box2d and maybe a bit more mature. So I ported that and got it working with the marbles demo. I was worried about performance, especially since bullet uses floating point instead of box2d’s fixed point and my phone doesn’t have hardware float. But it was fine, and it allows me to march ahead with bullet for both 2D and 3D physics.

Now, doing this all in Eclipse using Android’s plug-in and the CDT for the native code has been generally a good experience. There are a couple of things that are still needed. One is a way to automate the steps adding the CDT nature and builders to Android. And there are some things that don’t work. CDT’s scanner discovery, which scans build output looking for include path options, no longer works for my projects since I upgraded to CDT 6.0.1. Setting it up for cross compilers has always been a pain, and now it just seems to not work :(.

The other thing that bugs me now, is something that has always bugged us in the CDT community, and despite raising several bugs, has never been satisfactorily addressed is the Eclipse build system. I’ve set my Android project to reference the physic engine library project to control the build order. But when I go to clean my Android project, which is small, it cleans the referenced projects too, which aren’t so small. What makes it worse is that it kicks a rebuild right away so you can’t just clean your project and leave it that way.

Hopefully with the new openness shown by the platform team we can get something done there. But we’re all a little jaded from the history and we need to overcome that first.


