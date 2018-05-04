---
layout: post
title: Flash on the Brain
date: '2008-05-07 10:24:00'
---


I hate it when that happens. A shiny object flies by and I can’t sleep until I catch it. So I was up until 3 a.m. last night trying to figure out what Adobe Air/Flex/Flash/ActionScript was all about. It’s actually pretty interesting stuff technically. But as a number of people commented when I brought it up a couple of days ago, you do get the sense of vendor lock in, at least for now. But the specs are all open now, so open source implementations of this stuff at least have a fighting chance.

So why do I care about Flash (other than my insatiable need to learn as much as I can about the software industry)? Well, it fits in with my interest in mobile devices, especially those based on embedded Linux. As these devices get more powerful and have bigger screens, the line between laptop and mobile device is going to blur. And I think the expectations of users on the UI for these devices is going to grow as well. Everyone oos and ahs over the iPhone UI. It’s setting the bar.

But looking at a traditional embedded Linux box with a UI, does it make sense to run X Windows on it? X is horrible and antiquated. And it’s very hard to build flashy (sorry about the pun) UIs with it. It certainly wasn’t intended for resource constrained devices. Mind you the old X Terminals were pretty much embedded devices, but then where are they now…

So what are the alternatives? [DirectFB](http://www.directfb.org/) looks very promising and is growing in popularity in the embedded world. It gives you an nice API over the graphics hardware and input devices that let you build your UI as low level as you need. But it does require you to build a UI from scratch.

So this is the architecture that piqued my interest: Adobe AIR (which include Flash and the WebKit browser) running on DirectFB. Which then opens up other interesting architectures. Like mobile devices turning into web appliances that let you work connected or disconnected (is there a Flash office suite app?). And with Flash’s animation, video, and audio capabilities, you could build a pretty lively UI. And, from what I hear, there are a lot of graphic artists who have learned Flash who could give us a hand.

Now, I have no links to Adobe and this only crossed my mind as they “opened” up the technology with the [Open Screen](http://www.adobe.com/openscreenproject/) project. But if this move helps them build momentum in the mobile space, it opens up a lot of opportunities for mobile software developers, and graphic artists for that matter…


