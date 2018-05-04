---
layout: post
title: Qemu 0.10.0 now available
date: '2009-03-04 22:11:00'
---


[In a message from Anthony Liguori to the qemu-devel mailing list](http://lists.gnu.org/archive/html/qemu-devel/2009-03/msg00154.html), “The QEMU team is pleased to announce the availability of the 0.10.0 release. This release has been a year in the making and is the result of almost 3,000 changesets from around 80 developers.” The release was quickly put together in the last few days (i.e. in Eclipse terms, there wasn’t much of a ramp down). And the resulting build is actually pretty hard to find, at least until it gets propagated to all the mirrors, but it’s a milestone anyway.

There’s a pretty long list of new targets and hardware emulation. There’s also improvements to the VNC support. The biggest news is the new code generator for translating op codes into runnable code. It’s called TCG (Tiny Code Generator according to Wikipedia) and removes the dependency qemu had on gcc 3.x, which means it gets to take advantage of the huge performance improvements of gcc 4.x. I think I read somewhere that the Android qemu was running 1.5 times faster thanks to that. And my copy is humming using the gcc 4 I’m integrating into the future Wascana 1.0.

This release is a good sign that the qemu developers are getting serious about formal releases. It’s been quite a while since the last release and there has been huge architectural change. That has led to a some difficulties co-ordinating with the other projects that use it, like the kvm Linux virtualization platform. Having quality releases more often will make it easier to get changes from forks into the mainline, which is good for everyone.

For me, it’s just good fun to be able to have a virtual platform to try different ideas with C/C++ libraries that target mobile devices that I could easily target to real hardware some day. And I think it’s intriguing the Eclipse integrations we could do to make it easier to work in that environment. A lot we have already, like CDT (of course) and the Remote System Explorer for launching, and there is work on more coming from the [Tools for mobile Linux project](http://www.eclipse.org/dsdp/tml/). Interesting indeed.


