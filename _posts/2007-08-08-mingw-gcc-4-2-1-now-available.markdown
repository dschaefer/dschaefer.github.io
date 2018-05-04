---
layout: post
title: MinGW gcc 4.2.1 now available
date: '2007-08-08 22:55:00'
---


Danny Smith from the [MinGW project](http://www.mingw.org/) has posted his work on porting gcc-4 to the MinGW platform. From the mingw-user mailing list, it looks like a lot of people were waiting patiently for it. One thing I’ve learned in my days working in open source, it really makes you mad when someone complains that a release or some feature isn’t ready yet. But, I know I’m glad it’s finally here, even if it is currently experimental (with the target of 4.3 being the official version).

So what’s the big deal with gcc-4 versus gcc-3? The biggest thing is a new optimization framework which promises to be able to generate faster code even accross functions. This is an area where commercial compilers excel. And gcc-4 brings MinGW into the mainstream being releases only days after the official 4.2.1.

The other interesting thing is that the port also supports [OpenMP](http://www.openmp.org/), a standard API and language extensions to support parallel programming. I know the [PTP people](http://www.eclipse.org/ptp/) will be very interested in that. Also, there is support for Objective-C++, which we’ve had numerous requests to support with the CDT.

I’ve started updating the Wascana installer to include this new compiler and a couple of other updates it requires. [Tune into the web site](http://wascana.sourceforge.net/) to find out when 0.9.3 will arrive (with all it’s fancy new branding too 🙂


