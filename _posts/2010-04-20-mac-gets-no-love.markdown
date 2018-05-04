---
layout: post
title: Mac gets no love
date: '2010-04-20 09:12:00'
---


I should blog more. But twitter is so much faster. At any rate…

@timbray tweeted yesterday “Eclipse SPOD DIAF.” After getting out my magic decoder ring, I soon learned that he was complaining about the performance of Eclipse on Macs. Apparently there were memory issues in Eclipse 3.5 Cocoa that causes a lot of garbage collection (assuming I’m interpreting that correctly). That causes the pause icon to pop up while Eclipse is locked down. The so called Spinning Pizza of Death, which is being asked to Die In A Fire, or at least so my magic decoder ring told me. Kids and their fancy lingo…

I hear that’s fixed in Eclipse 3.6 and I haven’t seen it in the few times I’ve run Eclipse Helios on Mac. But it’s another episode in a long story of Mac not getting any love from the Eclipse community, or at least the contributors. The good news is that as more and more contributors are using Macs, these issues are getting addressed. But the perception has already been set free that Eclipse sucks on Macs and hopefully the Mac users are passionate about Eclipse to give it another try.

I ran into another case that confused the hell out of me last night. I was testing the new Android CDT integration I’m contributing to the Sequoyah project and had an NPE show up. So, as I do on Windows and Linux, I quickly tried to fire up my CDT workspace to take a look at the line of code the log was complaining about. You know, if you have an Eclipse running and you try to launch a second instance, it just pops up the one you have running.

From what I’ve been told, Mac applications are always singletons. You run one instance of the application and it’s able to handle multiple documents. But that doesn’t work in Eclipse because Eclipse can’t handle multiple workspaces. I remember that coming up at the e4 summit as someone wanting to do that, but at the time I didn’t get it. Now I do.

I imagine things like this will get solved over time (although the multi-workspace thing, I’m not sure). But it is a great example of how open source projects work. The only way features get done is if someone has a vested interest in getting it done. To date, there have been few Eclipse contributors with such an interest in Eclipse on Mac. Yes, that’s changing, but pretty slowly.

Now, here comes the controversial part. What you don’t see in open source much except for the few cases where projects are bankrolled by forward seeking companies with lots of money (i.e. Google) is projects investing before the need. We’ve known for a long time Mac was going to be important, the trends were pretty obvious. But open source doesn’t work that way. The funding for development isn’t strong enough to support risk like that.

Or so I think. I am curious if you agree and if you have a theory of why that is. I’m not sure how it can be changed, or if vendors who fund open source want it to change. I know of companies that don’t want it to. But the companies that do easily trump that if they can figure out how.


