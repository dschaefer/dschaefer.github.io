---
layout: post
title: Way too much fun with qemu
date: '2009-03-01 14:34:00'
---


As I’ve been blogging about lately, I’m getting ready for my EclipseCon tutorial which will walk the attendees through adding support for a cross-compile environment to the CDT. The target of this environment will be qemu running a tiny Linux platform which includes the latest release kernel, busybox, dropbear with sftp-server from OpenSSH, using the free glibc C run-time and gcc cross compile tools from CodeSourcery.

I’m using the default ARM target for the latest qemu which unfortunately has a bug in the FIFO emulation that interfaces with the emulated SecureDigital card where I want my root file system. I asked on the qemu-devel list and someone there sent me a patch they had posted a couple of weeks ago. Checking out the qemu source from svn into the CDT, I was able to fix up the function where this was done and I was quickly up and running with my root file system on the SD card image. Very, very cool!

The next highlight was when I got the ssh components running and I was able to connect to the qemu target using the Remote System Explorer from the Eclipse Target Management project. Also, very, very cool. I want to use RSE and the CDT remote launch to get the results of the build up and running on the target.

So now that I know how to build stuff from the command line, the next step will be the meat of the tutorial, creating the managed build integration for the cross compiler. Of course, you’ll have to come to the tutorial to see the result, and actually work with me though the process. But it should be fun!

And now that I’ve actually started working with qemu in the CDT, I’m starting to get that itch to add 3D graphics support again…


