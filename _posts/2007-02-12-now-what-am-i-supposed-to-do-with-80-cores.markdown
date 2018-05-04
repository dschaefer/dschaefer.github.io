---
layout: post
title: Now what am I supposed to do with 80 cores?
date: '2007-02-12 09:36:00'
---


Yesterday, Intel announced a research project they’ve been working on to produce a core capable of reaching teraflop (a zillion floating point operations, or something…) performance. The chip they’ve come up with has 80 cores. Sounds like a lot, and it is. Now, this is a research chip and it is missing things like a memory controller which makes it impractical for anything. But it is serving it’s purpose of helping us understand what such an environment of the future would be like. The benefits will be paradigm shifting, but we have a long way to go before we get there.

Of course, being a tools guy, I think the tools industry needs to jump on this. Without proper tools, developers just won’t be able to deal with the complexity of the software that takes advantage of such scalability. This is one of the reasons I’m very interested in the [Parallel Tools Platform](http://www.eclipse.org/ptp/) (PTP) project at Eclipse. They are trying to deal with such environments today by providing tools that support developers working with supercomputers used for scientific research.

The challenges are enormous and include the whole edit/build/debug programming cycle. What libraries and programming language enhancements do you need to write an 80 thread or process application, how do you build and deploy such a thing, how do you debug it? I can still picture the problem of setting a breakpoint, having 10,000 threads hit that breakpoint and then trying to find the one that you are interested in. Sounds impossible. But there are some pretty smart people working on PTP and it’ll be very interesting to see the solutions they come up with.


