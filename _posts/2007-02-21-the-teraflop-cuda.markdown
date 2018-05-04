---
layout: post
title: The Teraflop 'CUDA
date: '2007-02-21 11:51:00'
---


It’s interesting how the big vendors play off each other when some cool new idea gets close to becoming product. The latest one was Intel with their [80 core research chip](http://cdtdoug.blogspot.com/2007/02/now-what-am-i-supposed-to-do-with-80.html) for highly parallel teraflop computing. Now we see NVidia has released their [CUDA SDK and C-like compiler](http://developer.nvidia.com/object/cuda.html) that does the same with their latest 8800 series video cards.

Apparently, you can get 520 gigaflops (billion floating point operations per second) with their top end 8800 card which features as many as 128 single precision floating point cores. Combine two such cards in an SLI configuration and you can hit the teraflop mark, theoretically. They have a compiler that compiles programs written in C with some CUDA specific extensions that gets downloaded to the card which runs as a co-processor to your main processor.

I can see the applications for such technology being pretty much limited to scientific simulation type things, not general purpose computing, at least not in the short term. The main issue is that not every will have these specific cards in their systems, and it really is NVidia specific. But it looks like they’ll provide a huge amount of horsepower at a decent cost.

One of the reasons I blog about these things, other than I think they’re cool, is to show that C/C++ development is still alive and well and growing. I remember seeing a study a couple of years back that showed it on the decline with everyone moving to Java or .Net. But there will always be applications that need to run as close to the hardware as possible to run efficiently as possible, either because the computing resources are limited such as with mobile devices, or because they are very specialized such as the NVidia processors. Languages such as C and C++ that compile directly to executable object code is still the best way to achieve these efficiencies, and why we see the CDT as popular as it is.


