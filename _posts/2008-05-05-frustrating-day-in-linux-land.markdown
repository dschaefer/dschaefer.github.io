---
layout: post
title: Frustrating Day in Linux-land
date: '2008-05-05 21:40:00'
---


So I’m busy working with my team at Wind on some new installer work and I need to set up ClearCase to get access to the bits that go into the install. I have this spanking new machine, Quad-core Intel, 4GB RAM, 750GB drive. I really got it so I can run multiple virtual machines on it for testing. But if I could run ClearCase on it too, then I could use it for install builds too.

But my issue is that ClearCase is only supported on certain enterprise versions of Linux. But I want to try the latest KVM support in Ubuntu. So I first installed Ubuntu 64-bit and gave it a try. Ubuntu’s 32-bit support in 64-bit installs is horrible. You have to manually install the 32-bit libraries. That probably should be automatic, but then they are trying to fit on a single CD so maybe it’s too much. Unfortunately even with the 32-bit libraries, the perl engine ClearCase ships with crashes. So forget that.

So next up, I tried Fedora 8. It’s much closer to the supported Red Hat Enterprise and might have a better chance. And besides, there are some good Eclipse guys at Red Hat and I should be supporting them. The 32-bit libraries were automatically installed (but then it is a 3+ GB DVD). So I got a lot farther. After tricking the ClearCase install scripts into accepting Fedora as a “supported” kernel, I got as far as building the MVFS kernel module.

As I tried to fix those errors, I started to feel like I was porting their module for them. And it was a lot of work. We were going from version 2.6.18 of the Linux kernel to 2.6.24, but given how many APIs changed, it felt like I was going to 3.0 or something. At any rate, it doesn’t feel like something I should be investing my time in so I gave up on that.

So I tried the supported RHEL 5. You know what, after installing it and rebooting it. No network. RHEL 5 didn’t have a driver for the ethernet on the new machine. For crying out loud (again…). Unfortunately, it’s back to Windows for me. At least for now. Hopefully I can tweak ClearCase to make it fast enough to be usable.


