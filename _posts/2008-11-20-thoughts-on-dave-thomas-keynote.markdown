---
layout: post
title: Thoughts on Dave Thomas' Keynote
date: '2008-11-20 07:51:00'
---


[Ed Merks already gave a summary](http://ed-merks.blogspot.com/2008/11/dave-thomas-keynote-focused-on-history.html) of Dave Thomas’ keynote yesterday morning here at [Eclipse Summit Europe](http://www.eclipsecon.org/summiteurope2008/). It was the first time I saw Dave speak and I was warned he tended to say things that offended the audience. And to Dave’s point, that is kind of what a keynote speaker should do. Spark thought. Break through the assumptions that we tend to fall into when we get comfortable in our skin. And I think he raised some serious points that are making me wonder about what’s really happening in our industry.

I guess his main point is that Java for embedded has missed the boat. If you haven’t gone through the pain of doing Java for embedded devices, don’t worry, you didn’t miss anything. I’ve been waiting to see when I need to care about Java in this space and I’ve talked to some of the people here at Eclipse Summit Europe about this. I think they quietly agree with Dave. Those that have figured out how to do Java on embedded are doing OK with it. But there are a lot of issues to face. The worst of them is the bloat that the Java VM continues to grow from release to release. The embedded VMs are horribly crippled, and if you want to use the Sun VM, you are crippled from paring down that bloat. The discussion is interesting, and we may still be proven wrong, but for now, I can ignore Java for embedded and I can sleep at night.

There were some other messages from Dave that hit home as well. Programming is horribly complicated. Normal people will never be able to figure it out. Which means if you have figured it out, you’re not normal, and I guess that includes me. But it is true. I’ve blogged a lot about this in the past. We can barely get our programs to work as it is. Wait until you’re trying to program 100 threads running through your mess all at the same time. We’re doomed.

But there are some things we can do to give us a chance to survive. Dave talked a bit about how the lack of a software component model is making us look like fools in the eyes of the engineering community. Can you imagine if automakers had to custom build all the components that make up a car? Imagine now if we could go to a shop and pick up high quality software components and tie them together will few lines in a script.

Now Dave was be extreme in his position. There are a number of areas where component models are being used, OSGi is an obvious one, all these “Mash-ups” are doing things like this. But coming back to embedded, we can’t rely on Java to provide the solution. Dave’s answer was C++ with JavaScript. And I think that’s a great idea. Build components in C++ and tie them together with a scripting engine. Dave picked JavaScript, which is OK but he did mention he’s working with Google on their V8 JavaScript engine. Lua is another good choice. And actually Domain Specific Languages offer solutions as well (and I’m not just saying that because I’m sitting in Rich Gronback’s DSL talk right now ;).

It was really interesting to spend time with Dave Thomas in his keynote and with a group of us at the hotel bar. I could learn a lot from him. This week it was to open up my mind and challenge the assumptions. If you read this blog regularly you find that I tend to do that anyway, but it’s an important reminder to keep doing that and make sure we don’t make the same mistakes over and over again.


