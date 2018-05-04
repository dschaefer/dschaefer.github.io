---
layout: post
title: Taking the Long Way 'Round
date: '2017-07-27 14:42:05'
tags:
- eclipse
---


Remember [Eclipse Two](https://cdtdoug.ca/what-is-two-much-more-than-yet-another-eclipse-ide/)? Yeah, that was a lot of fun. Not sure anyone cares what happened to it. It made quite a splash back at the beginning of the year which proved to me that there is interest in a new tools platform for the desktop. Well, it’s been an interesting journey since then and I thought I’d give you an update.

First, I do firmly believe that Electron as a combination of Chromium for UI and node.js at the core will be a great tooling platform for the future, if not sooner than that. You look back when Eclipse started, and I think Mike mentioned this in a recent article, Java was the cool new kid on the block. Everyone wanted to learn it and use it and with SWT, it finally became performant and good looking enough to build the next great IDE platform that we have today.

You look around today, and ask that same question. What is the cool kid on the block that everyone wants to learn and work with? Well, I think it’s obviously HTML5. There’s no doubt there’s lots of hype to it. And with hardware accelerated rendering in Chromium and the native look and feel you can get with Electron, I think it’s ready to be the next next gen.

But a funny thing happened along the way. We released our latest QNX Software Development Platform with the culmination of all the work we’ve done the last few years with our Eclipse-based IDE Momentics. And our customers like it. They like it a lot. CDT is still the best C/C++ IDE in the industry and the user experience improvements we and the rest of the Eclipse community have delivered is paying off for us and them.

As much as I’m interested in seeing the next generation IDE platform, it has to be as good or better than what we have today. And personally, I think we’re a long way from that. Knowing how much work that has gone into the CDT to have it’s great static analysis engine and it’s clean debugger integrations and the clean up of launch workflows that we’ve achieved with the Launch Bar, you would need a very strong community to duplicate that. And you would need community leadership to bring all the different interested parties together to work towards a common goal. I struggle to see how that comes together and I look forward to discussing with fellow CDT’ers at EclipseCon Europe to understand where their visions lead.

For now, along with working on improvements to Momentics and CDT, I am continuing to work with Electron on some other tooling ideas. I think we have something cool in the works for system tracing, an area that a lot of us embedded systems vendors have struggled with in Eclipse and SWT. A lot of custom code has been written to make our System Profiler and Eclipse’s Trace Compass look good and navigate well. That could be an area where we could grow a community.

It will take us a long time before we know where to go next and I’m convinced that’s a good thing. If anything my work on Electron-based tooling has taught me is that we have a lot to learn with these new technologies. They are so new and constantly changing. It’s tough to build an IDE platform for the next twenty years when JavaScript frameworks come and go every couple. But the good news is that we have time. Eclipse is still going strong and giving our customers the great user experiences and the productivity improvements we promised them. We can afford to be choosy on the next one that will give them the same.


