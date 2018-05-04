---
layout: post
title: Visual Programming for Multi-Processing
date: '2009-11-09 20:42:00'
---


I spent a little time on the weekend taking a deeper look at the Unreal Development Kit (www.udk.com), and I continue to be shocked that they are giving out all this great technology to you and me to play with. And it really blew me away when I saw their Materials editor. There’s a tutorial here, [http://udn.epicgames.com/Three/MaterialsTutorial.html](http://udn.epicgames.com/Three/MaterialsTutorial.html).

Take a look at how you program the materials algorithms. You lay them out graphically and hook up data flows between components. The order of execution or the parallelization of the algorithm is automatically inferred by the declarative nature of the model. When you’re ready, these get generated into optimized shader programs that download to your graphics card when drawing the 3D models that these materials wrap. Very cool and very efficient.

This is very similar to what I found with the SynthMaker program that came with the FL Studio audio workstation software I’ve been playing with too. There you define the algorithm for software DSPs and GUI controls that change values using the same paradigm.

To see it in two places now, I’d love to have this available to the general public for any kind of application. Would it really be more efficient to write general multi-threaded and multi-process algorithms that way or would the modeling tools get in the way. Epic and SynthMaker felt it was right for their users, is it right for everyone? You know, I bet we could build this using Eclipse modeling tools and try it out…


