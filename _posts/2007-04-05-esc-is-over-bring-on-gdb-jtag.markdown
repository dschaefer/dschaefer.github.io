---
layout: post
title: ESC is over, bring on gdb JTAG.
date: '2007-04-05 19:33:00'
---


Well, my talk went pretty well. I think i had over 75 people there. I stopped counting at 60 and people were still filing in the door. You have to get your badge scanned to enter the room which took some time. But the audience was very attentive and had some great questions and feature ideas. Unfortunately I didn’t capture them all, so if you were there and had an idea, please raise a bug for it :).

One thing a few people asked me about this week was the [Zylin Embedded CDT](http://www.zylin.com/embeddedcdt.html) plug-in that a few vendors are starting to use in their commercial products. It essentially supports debugging using JTAG devices that use gdb as their debug engine. Those who have been around for a while have heard of Øyvind from Zylin who has been trying to get his changes into the CDT proper. For various reasons, those changes have been rejected.

But I think it’s time to take a serious look at this and see if we can address his issues while maintaining current functionality. Having forks of the CDT is bad for the community, and is really bad for those vendors that have to use them because it has the potential to limit further integration possibilities, especially if APIs are changed. The objective should be to make everyone happy. Sometimes that’s not possible, but in this case I think it is. And I’m making it my mission for the rest of CDT 4 to do my best to make that happen.


