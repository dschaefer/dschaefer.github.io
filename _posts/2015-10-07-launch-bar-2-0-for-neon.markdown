---
layout: post
title: Launch Bar 2.0 for Neon
date: '2015-10-07 16:57:16'
tags:
- eclipse
---


[![Screen Shot 2014-03-14 at 10.08.11 AM](/images/2014/03/Screen-Shot-2014-03-14-at-10.08.11-AM.png)](/images/2014/03/Screen-Shot-2014-03-14-at-10.08.11-AM.png)

I’ve been working on the Launch Bar for it seems like forever. But it’s still only used by a few people in the Eclipse world and I haven’t really made a push to get others to adopt it. I don’t think it’s quite ready for that. I’ve really been struggling with it’s place in Eclipse. It fills a missing need as far as improving the Launch experience.

It’s also filling a missing API need, the ability to specify where you want to Launch to. And I’m now thinking that this needs to be directly added to Platform Debug so that the launch target is passed on to the launch configuration delegate so it can pass it on to the launch, build for launch, etc. And if we’re going to do that, we should really put the launch bar down into the Platform Debug as well.

And if we’re doing that we should really not be using IRemoteConnection as the launch target as the Launch Bar does now. I’ve received a number of requests to generalize the target concept since not everyone gets why they need to use the new remote system. It’s funny as I actually had started with a more general concept anyway. So I’m going back to that.

But it does mean there will be API changes so the Launch Bar for Neon will be a major release, 2.0. The end goal is to contribute it to Platform Debug but I won’t have time for that in Neon. But we will get the APIs in shape so it’ll be ready for Neon + 1.

In the meantime, I have a release of the Arduino C++ IDE to put out which does use the Launch Bar. I’ll be producing a video of how to use it and I think from that you’ll see the value the Launch Bar really adds, especially when you have multiple targets where you want to launch your application.


