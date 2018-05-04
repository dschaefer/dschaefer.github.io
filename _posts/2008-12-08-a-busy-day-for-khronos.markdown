---
layout: post
title: A busy day for Khronos
date: '2008-12-08 22:15:00'
---


My [Khronos.org News](http://www.khronos.org/) feed filled up all of a sudden today. Looks like they’ve been busy and had a couple of announcements to make.

They released [a new version of the 2D OpenVG spec](http://www.khronos.org/news/press/releases/openvg_1.1_specification_publicly_released_by_khronos/). They added some APIs for text glyphing to make it easier to draw good looking text. I’m not sure anyone really uses OpenVG, especially when you are most likely to be drawing 2D in a web browser with Adobe Flash or SVG (and even then, most likely Flash). From the news release, this is probably most interesting to the mobile crowd.

The more interesting announcement for me was [the release of the first OpenCL spec](http://www.khronos.org/news/press/releases/the_khronos_group_releases_opencl_1.0_specification/). OpenCL is a standard for running general algorithms on the newer GPUs in video cards. It’ll also be ported to other multi-core systems like Cell and DSPs, but most likely you’ll be using it with a video card. Of course AMD and nVidia were quick to announce their support for this spec, which gives it some immediate momentum.

OpenCL specifies a C-based language for parallel processing as well as APIs that drive them. Up until now, nVidia and AMD had proprietary solutions that didn’t work cross platform. OpenCL opens the door to make parellel programming available to more and more programmers and I’m dieing to see what they’ll do with it…


