---
layout: post
title: Bug 160012 - The CDT Team at Work
date: '2007-04-27 09:03:00'
---


There have been massive changes in the CDT’s build system and the CDT’s New Project wizard. This is all great work that the gang at Intel in Russia have been doing to clean up the long standing weirdness of making the user pick between the two competing build systems in the CDT: standard vs. managed. The user still picks, but it’s much more subtle. Along with this, other components of the CDT can start getting more information about what the build system is doing so that we can do things like pick the default debugger based on the active tool chain.

Another component that we’ve been eagerly waiting for was the new project template support proposed by the gang at Symbian in London. This allows us to gather some information in the New Project wizard and generate source files and build settings based on a template. Now this proposal actually occurred pretty much in parallel with Intel’s build system work, and given that, they didn’t really take each other into account.

Well, once the build system was in place with M6 at the beginning of April, it was time to mesh them together. I am thrilled with how this has worked out. It was not an easy task as we had to undo assumptions that had been made. Not to mention the time frame was short with feature freeze being this weekend. But it was great to see how well the two groups worked together along with the odd input from us over here in North America. To see for yourself, check out the [bug report for 160012](https://bugs.eclipse.org/bugs/show_bug.cgi?id=160012) where the discussions happened. At last count, there were a 110 comments on it, some of them pretty lengthy.

I’ve done “around the world” development in a commercial setting but never at this level and never this successful. Every morning, I wake up and sift through a pile of bug updates that my friends in Europe and India have sent out. We then get a few hours where we’re actually at work at the same time and the bug traffic is pretty heavy in the morning. But then tails off towards the end of the day. You always have to think about what time it is elsewhere (even though someone may still be working late – go to bed Mikhail S! :).

I think that it’s a sign of a successful open source project when you have contributors from around the world with diverse needs but all fighting through the time differences to work together for the common good of the project. This is really the main reason I love working on the CDT. Helping create the world’s best and hopefully soon, most popular, C/C++ IDE is pretty good too…


