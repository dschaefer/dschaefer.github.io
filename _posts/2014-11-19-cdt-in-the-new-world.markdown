---
layout: post
title: CDT in the New World
date: '2014-11-19 12:12:27'
tags:
- eclipse
---


An interesting thing happened the other day which I think shakes some of the foundation I’ve had in my mind about the CDT. My vision was always for CDT to support C, C++, and related languages on every platform. And that has always included Windows. Mind you, we’ve never really done a great job there but we do have lots of users using it with Cygwin or MinGW and you can argue how well they support Windows application development.

The big news was Microsoft’s Visual Studio Community Edition which is a free version of their complete IDE for individuals and small teams. This is different from their Express editions which were severely limited in the end, including lack of 64-bit support, and the inability to install plug-ins into the IDE. No, the community edition is the full thing and is a pretty important step for Microsoft as they try to keep developer interest in their platform.

As long as Microsoft charged money for Visual Studio, I always thought CDT had a play. I’ve done a little work on supporting integration with their Windows SDK (which includes a 64-bit compiler) at least for build. Debug was always a big hurdle since you’d need to write a complete debugger integration that is very different from gdb. So, really, this integration barely worked. And now that VS is essentially free to the market we serve, there’s little point at continuing that effort. The same is essentially true with Objective-C support with Xcode on Mac, which even they are drifting away from to focus on their new language Swift.

But you know, despite giving up on a dream, I think CDT has an important role to play in it’s field of strength, i.e. support for the GNU toolchain, especially as used for embedded development with it’s new found focus as a pillar in the Internet of Things. As I’ve talked about on Twitter and on CDT forums, I am working on a CDT integration to support building C++ apps for Arduino. Once that’s done, I’ll shift focus to a more complicated environment around Raspberry Pi which I hope to add better remote debug support to CDT. Yes, I know everyone loves to talk about using scripting languages on the Pi, but I want to expose these hobbyists to the real world of embedded which is almost exclusively C and C++, and get them started using CDT.

I still haven’t given up on the desktop, at least desktop support with Qt. I really want to make CDT a first class alternative for Qt development. We have a good start on it and will continue with things like a project file editor, easier setup of builds, and import of projects from Qt Creator. The great thing about Qt is that it also is truly cross platform, allowing you to write your app to run on the desktop and then migrate it to your embedded device, such as the Raspberry Pi. And supporting both of these with the same project is one thing CDT is pretty good at, or at least will be once we fix up the UX a bit.

In the past, much like the rest of the Eclipse IDE, I think we on the CDT have focused a lot on being a good platform, almost too much. While vendors have done a great job at bringing the CDT to their customers writing for their platform, including my employer :), aside from the Linux community, few of us work on supporting the direct user of the Eclipse C/C++ IDE. I think focusing on CDT’s areas of strength and targeting specific open environments and not chasing dreams will help me contribute to the CDT in ways that will actually help the most people. And that’s most satisfying anyway.


