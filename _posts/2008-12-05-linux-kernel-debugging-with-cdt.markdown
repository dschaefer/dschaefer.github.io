---
layout: post
title: Linux Kernel Debugging with CDT
date: '2008-12-05 11:28:00'
---


Just ran into [this awesome tutorial](http://issaris.blogspot.com/2007/12/download-linux-kernel-sourcecode-from.html) on how to use the CDT for debugging the Linux kernel using qemu’s gdb remote debug service that makes it work much like a standard hardware/JTAG debugger.

This was something I played with a while ago when I looked at adding hardware debugging support to the CDT as an optional service. And I believe Elena from QNX has continued on with that work and we should hopefully see it completed for Galileo (if not before that).

But it further solidifies for me how important [qemu](http://bellard.org/qemu/) is as a tool in the belt of the embedded software developer. We’ve seen it as a key enabler for Android without which I’m not sure it would have achieved the momentum it has. I think there are still issues with it, and of course one I’m looking at is ease at adding new hardware emulation and 3D graphics support. But I think there is plenty of opportunity there and being an open source project, the door is open to help make that happen.


