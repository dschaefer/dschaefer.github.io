---
layout: post
title: SystemC/qemu - Three Worlds Collide
date: '2006-11-22 10:16:00'
---


[Way back in February](http://cdtdoug.blogspot.com/2006/02/systemc-two-worlds-collide.html), I wrote about a really cool hardware description language called SystemC. It is essentially a C++ library that allows a programmer to model hardware concepts and included a run-time that simulates the hardware. This is one of the reasons I love C++, you can use templates and overloads and inlines to bring the abstraction layer up a few notches, essentially defining a new language, without having to build a new compiler. And it usually optimizes out to something very fast.

I’ve also been following the development of [qemu](http://cdtdoug.blogspot.com/2006/10/qemu-my-favorite-tool-of-week.html), a processor emulator that runs on multiple targets and has extensibility to add emulation of peripherals as well. And, if you have a fast machine, you can almost get the same performance as the real hardware. The best thing I see about qemu is that it really lowers the barrier of entry for people who want to try out embedded development without having to spend real money on real hardware. And it is much easier to carry around to trade shows :).

Well, if you have two very cool simulation/emulation environments, wouldn’t it make sense to combine them? Of course, and that’s what a group from the Universitat Autonoma de Barcelona have [done](http://cephis.uab.es/proj/public/qemu/). They have implemented a bridge that appears on the qemu PCI bus for drivers to access and passes signals back and forth to the SystemC design. It’s a great idea and really opens the door wider for hardware/software co-design.


