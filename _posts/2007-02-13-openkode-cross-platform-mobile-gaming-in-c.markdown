---
layout: post
title: 'OpenKODE: Cross Platform Mobile Gaming in C'
date: '2007-02-13 11:31:00'
---


I blogged a while back about an open source mobile gaming device, [the GP2X](http://www.gp2x.com/). It’s a pretty simple and inexpensive unit with a dual core ARM configuration. I think a lot of people are using it for simple 2D games and there are ports of the arcade machine simulator, [MAME](http://www.mame.net/), to it. It’s not a very powerful machine, but I thought the idea was pretty powerful.

It got me thinking about whether the industry would be interested in a similar platform but with 3D gaming support. And if not, why not. Maybe these things cost too much to build. Maybe the business case isn’t there. I haven’t seen too much interest from the big gaming houses on porting their titles to OpenGL ES, a standard 3D API for mobile. But then, there isn’t really a high volume platform out there that supports it to the scale of the Sony PSP and Nintendo DS. Unless you count phones, but you can’t do serious gaming on a 1″ screen…

But it looks like the gang at Khonos.org are trying to do something about that. They recently ratified a draft specification for a common platform API called [OpenKODE](http://www.khronos.org/openkode/). It’s a collection of C APIs, most of which they’ve already specified for video and audio. But it also has a OS abstraction layer so you can compile applications against any OS, or so goes the theory. The intent is to provide a platform for content providers that will allow them to hit as big a market as possible.

They are accepting comments from the industry and I see vendors starting to do press releases announcing support for it. My hope is that you’d start seeing mobile gaming platforms like you see with MP3 players, i.e., a lot of vendors making different types of devices but all supporting common standards. That would sure change the face of the industry a bit.


