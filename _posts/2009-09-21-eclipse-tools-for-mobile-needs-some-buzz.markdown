---
layout: post
title: Eclipse Tools for Mobile Needs Some Buzz
date: '2009-09-21 14:39:00'
---


I attended my first Sequoyah (Eclipse tools for mobile, except J2ME, but that’s another story) meeting today. Why am I? Well I’m getting more and more into mobile app development in my hobby time, at least for Android anyway, and I’m turning that into a personal focus on better support in CDT for mobile application development. We can then make this available for platform vendors who want to better support developers making applications for their platforms.

My plan is to start by building a set of plug-ins that automate at least the build setup for Android JNI development. Debug is another story and maybe someone else can help with that. And we can look at what’s needed for other open source mobile platforms down the road as well. And maybe some other vendor will come along and help out.

But, as I dig into what’s happening with mobile at Eclipse, I’m a bit surprised, and disappointed, about how little there actually is. Motorola is putting forth a great effort and contributed a significant amount. As with most vendors (almost all) that contribute to Eclipse it is mainly focused on their own commercial needs. But they also don’t seem to be getting much help from anyone else. It takes multiple companies to make a platform and it’s sad to see that isn’t really happening, despite all the marketing buzz surrounding Pulsar.

And I was also saddened to see Craig Setera’s blog for help for the Mobile Tools for Java project. MTJ is probably the project hardest hit from vendors coming and going that I’ve seen. And after the push to get Craig’s EclipseME project merged in for the reboot, I was hoping for greater things there.

On the Sequoyah call, I was asked for advice on how we could solve these things. Man, it’s tough. You really need a community, and in particular, a vendor community, that has a vested interest in contributing. We had it easy with the CDT. Everyone needed an extensible C/C++ IDE and it made business sense to invest a person or two to help make it happen. I had it pretty easy as a project lead, and I feel for Craig and the Motorola gang as they try to get this thing going.

The only thing I can come up with is a trick I used in the “dark” days of the CDT after my team at IBM were reallocated. “Create the need”. Find something that vendors will see the need to invest in. Usually, this is in the form of some platform piece that they know they need and that multiple vendors can work on, and then show that not enough people are working on it so it’s going to suck in their product too.

I’m not sure that’s going to work here since there seems to be a huge hesitation to make contributions from the vendors who could be contributing. But that was true with the CDT in the early days too. It was the QNX+Rational show for quite a while until Intel and TI broke the ice.

At any rate, I’m posting this as an attempt to help Eric C out. I’d really like to see Sequoyah succeed and for us to have a nice set of platforms and examplary tools for mobile app development at Eclipse. But that won’t happen without growing the community and we’d certainly be interested in your thoughts on how we can make that happen.


