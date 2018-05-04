---
layout: post
title: Another Awesome CDT Summit
date: '2008-10-02 19:59:00'
---


I just realize I haven’t blogged about our CDT Summit last week. Shame on me, because it was a great three days. It was smaller than previous summits, only 16 people. But this time, we didn’t have the guys there that were just lurking in person. Everyone was there representing real Eclipse contributions. So we ended up getting a lot of real work done.

We started on the first day by updating eachother on what we were planning for the next release, Galileo, which we determined by the end of the week will be CDT 6.0. It’s much more of a marketing number since I don’t anticipate huge API changes, but there will be some, especially in the build area.

We then talked a lot about development process and how we can improve the way we work on the CDT. It’s a challenge since many of us are only part time on the CDT. But we all agreed that becoming more formal in the way we do things is necessary and we have plans on doing just that.

The next day we broke up into two groups to do some deep dives into specific areas. One group dove deep into indexer issues. They talked a lot about some of the tougher areas that the CDT index and parsing technologies need to deal with, like C++ templates. The biggest new thing from them was discussion on how to represent inactive code, i.e. code that is ifdef’ed out given the current configuration. They settled on starting with doing so in the Outline View at least. Any more is a research activity.

The other group talked about debug. The biggest move there is the integration of the Debug Service Framework from the Device Debugging project into the CDT. I anticipate DSF will be the future standard debugger integration point for the CDT, and maybe even for the Platform. At the same time we will continue to support our existing CDT Debugging Interface (CDI) integrators. I’m also excited about the potential disassembly debugging editor that should hopefully make it easier to look at the object code being debugged.

On the last day we talked about e4 resources and the start of my straw man proposal I have put together. We also talked about the CDT build system, and in particular, the CDT project model that serves as the common model for them all. We’ve unfortunately lost the main developer of this work before it finished and we need to take another look at it and hopefully simplify it. It’s a good lesson that you shouldn’t be hands off if you totally depend on an open source component. The people working on that component may vanish and you have no way of getting fixes in.

I really wasn’t sure what to expect from this year’s summit. In many ways, the CDT is feature complete. And the plan will show that. But we still have a lot of usability and quality issues to address and the team is committed to focusing on that this year. And that will help solidify the CDT’s place on the developers desktop. And that was exemplified by Red Hat’s presence there. They are committed to making Eclipse the Visual Studio for Linux development. And that’s a good place to be.


