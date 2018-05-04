---
layout: post
title: OpenGL 3.0 or OpenGL ES 2.0?
date: '2008-10-09 14:49:00'
---


First, I have to admit, I’m a newbie at this whole 3D programming world. I watch from a far with a lot of interest but no real experience working in that world. So I apologize ahead of time if this is a stupid question. But I know a lot of CDT users are using the CDT to work with 3D graphic APIs and game engines so I thought I’d bounce this off you.

It was interesting to watch the response to the release of the latest major version of the [OpenGL spec](http://www.khronos.org/opengl/). The reception from the game development community was especially interesting. [They were furious](http://tech.slashdot.org/article.pl?sid=08/08/11/2135259&from=rss), at least according to Slashdot. But I can see disappointment in other articles I’ve read. The question came up: do we declare Microsoft the victor in the OpenGL versus [DirectX](http://msdn.microsoft.com/en-us/directx/default.aspx) wars? To which I add, does this spell the end of the dream of gaming on Linux?

From what I gather, there were a couple of issues with the OpenGL 3.0 release. One, the group writing the spec disappeared behind closed doors and sprung it on the world when they were done without really getting the ordinary game developer’s input. And in the end, it appears a lot of compromises were made to keep the non-game developer, the big CAD companies from what I hear, happy. So despite discussion of big architectural changes to compete with DirectX, it ends up not even worthy of the major version number.

It highlights the problem of trying to be everything for everyone and how that is impossible in many situations. Maybe the game developers need a special version of OpenGL spec’ed out just for them. If not, they’re all jumping on the DirectX bandwagon and see you later.

But that got me taking another look at [OpenGL ES](http://www.khronos.org/opengles/), the OpenGL APIs reduced for embedded applications and gaining wide acceptance in the smartphone market. It was interesting to see that the Playstation 3 uses ES as one of it’s available 3D APIs. And reading a few forums I’ve seen comments from experts who think OpenGL ES, at least the 2.0 version centralized around shaders, is OpenGL done right. The drivers are a lot easier to write and the API cuts out almost all the duplication and focuses on efficiency. It does make one think.

For the future of Linux gaming then, should we be looking to OpenGL ES? I don’t know how many OpenGL experts read this blog but I’d be interested to hear your comments on this. I recently bought a book on OpenGL ES programming to see what it was all about and it started to make sense to me that maybe this is the right direction. Heck, it almost seems like Khronos’s master plan…


