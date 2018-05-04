---
layout: post
title: Another legend has eyes on the future
date: '2008-09-15 21:55:00'
---


I just finished reading an interview with another legend of the game programming industry, [Epic’s Tim Sweeney (Mr. Unreal)](http://arstechnica.com/articles/paedia/gpu-sweeney-interview.ars). First it was [John Carmack from id (Mr. Doom)](http://www.tomsgames.com/us/2008/08/07/carmack_interview/) wondering how game developers will be able to harness multi-core technologies to improve game performance. Now I see Tim has a very interesting vision for how these technologies are going to change the industry.

It looks like both of them agree, multi-core general purpose processors will make graphics specific processing units obsolete, at least the fixed function parts of those graphics processors. But Tim seems to have a grasp of what that environment will look like. And it’s both exciting and liberating.

Essentially, he sees the return of software rendering, just like we had before the 3d hardware accelerator industry kicked in. Software rendering gives game programmers the freedom to implement whatever algorithms suite their needs, and they aren’t tied to the DirectX and OpenGL APIs which Tim says is really tying their hands. They can create whatever data structures they need to represent a scene and do whatever they want to slash that scene onto the pixels.

And he sees building that future with general programming languages and C++ in particular, instead of custom, hardware specific languages. Using C++, you have a shot at simplifying the programmers life, using the same technology for everything compute intensive. Game algorithms essentially come down to doing as many floating point operations at the same time as you can. Of course, this can be done in C++ with the right libraries, or even if necessary, a good compiler that can optimize your code to take advantage of whatever vectorizing capabilities your hardware has.

I anticipate this will be an exciting time for game engine developers. Certainly Tim seems pretty excited about it (and I highly recommend reading this article to catch some of that excitement.) And the good news is that we don’t need to invent new technologies to make it happen. C++ will do just fine (with a little help of the CDT, of course 😉


