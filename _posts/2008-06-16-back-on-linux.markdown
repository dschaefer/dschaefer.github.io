---
layout: post
title: Back on Linux
date: '2008-06-16 21:27:00'
---


I don’t know why I get the urge to blog about my Linux journey. I’m sure it’s not very interesting. But after a few days of working hard trying to set up ClearCase the way I want it so I can generate p2 repositories from our Wind River product release views, I’ve gotten back to why I was a *nix guy back in the day before Windows became a much better desktop.

I guess when you find a use for [cpio](http://en.wikipedia.org/wiki/Cpio), you are clearly destined to be a Linux junky. I’ve also fallen in love with NFS automounting (shh, don’t tell my wife, she’ll find that weird). When I can go ‘cd /net/yow-dschaefe-linux’ and get to my Linux box from anywhere on the WAN, that’s pretty cool, not to mention handy. Doing a ‘cpio > /net/yow-dschaefe-linux’ from a ClearCase view on a Linux machine in California to my box in Ottawa and have fairly decent performance, that’s the greatness of Linux file systems in a nutshell.

And using [KVM](http://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine) to set up a virtual machine to run the version of ClearCase I need and from there to NFS mount a directory from my real hard drive and then to do a ClearCase view export back to my real machine so I can run the generator at full speed, it just rocks. It’s not for the meek and it has taken me more time that I wanted to figure it all out, but Google is your friend and now that it’s set up, I’m ready to go.

So, yes, I still think Windows is the better desktop, but for file and compute servers, Linux is clearly the champ. But of course, you all know that already 🙂


