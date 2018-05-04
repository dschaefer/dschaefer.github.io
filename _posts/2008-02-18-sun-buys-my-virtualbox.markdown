---
layout: post
title: Sun Buys My VirtualBox
date: '2008-02-18 00:07:00'
---


One of the issues I have to deal with when building Eclipse-based software is the need to test on a number of different platforms. Yeah, “Write Once, Run Everywhere”, whatever. To build a proper IDE and especially the new Installer stuff I’m working on, you need to access the native platform. There’s no getting away from it. And with that, you need to deal with all the “special” behaviors that these platforms offer you.

And when you’re dealing with many platforms, it’s gets pretty expensive and noisy and hot to have all that hardware stacked in your office, so it makes a ton of sense to use software virtualization for test environments. I’ve mainly used vmware over the years but before going through the hassle of purchasing a new copy for my new job, I thought I’d try alternatives.

One I found that worked pretty good was [VirtualBox](http://www.virtualbox.org/) built by German company innotek. It’s got a weird license. It’s “Free for personal use”. It has an open source aspect to it but it’s a subset of the whole thing that’s free for personal use so it’s pretty confusing. But it performs really well, leveraging the virtualization hardware in new Intel and AMD CPUs. And has guest drivers that make the integration with the host work better too, just like vmware.

So today, I went to their web site to see if there was an update to the software and I found a link to this announcement: New Feb 12, 2008 – innotek to be acquired by Sun Microsystems. What?!? I thought this was just a small outfit that was building a nice VM for fun with hopes of making it big one day. Well, I guess they made it big. Congrats to them!

I’m not sure how to interpret Sun’s motives or what will happen to VirtualBox once it’s in their hands. But just like MySQL, I hope they keep the open/free aspects of it alive and well and invest in it to make it even better.


