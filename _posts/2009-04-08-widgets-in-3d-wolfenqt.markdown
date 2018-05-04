---
layout: post
title: 'Widgets in 3D: WolfenQt'
date: '2009-04-08 12:04:00'
---


As the shiny balls spin around in my world, Qt has jumped back into the foreground. My Fedora laptop is busy building 4.5 as I write this and slowly catching on fire (man these things get hot when they’re busy working). While that was going on, I took another look at how you’d implement Qt widgets in 3D space, kind of like Clutter does in a GTK fashion (mind you I think those are just static 2D images, not widgets).

Low and behold, I came across the [Qt Lab Blog entry by someone there](http://labs.trolltech.com/blogs/2008/12/02/widgets-enter-the-third-dimension-wolfenqt/) who actually has a demo of Qt widgets running in a maze similar to the old id games. He called it WolfenQt. Take a look here:

Very cool! This is exactly how I was hoping it would look and feel. And Qt has the framework to make it happen. I need to do some experimentation with it once I my 4.5 compiled to see how much of this is done in OpenGL versus software rendering. Looking at the code it looks like quite a mix of both. But from the video, it looks fast enough. And I do know the marching guy is rendered using OpenGL at least.

This is the kind of innovation I’d love to see. We talk a lot in the Eclipse world about Java thick clients and Browser/Server architectures. But there’s still so much more you can do using native APIs that take advantage of all the new hardware acceleration capabilities that today’s platform providers are giving us.

And the CDT is such a natural IDE for this new world. With all these new platforms, developers really need a cross platform cross target development environment to work with them all. The goal for my CDT work right now is to show that off and put together IDE packages, like Wascana and maybe something with DSDP for embedded, that can be used in these environments.


