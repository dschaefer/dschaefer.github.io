---
layout: post
title: A lesson in scalability
date: '2007-08-20 15:57:00'
---


I just read the [Skype blog](http://share.skype.com/sites/en/) where a Skypian describes (well glossed over, but we get the gist) what happened with their two day outage last week. I don’t use Skype very much but I know a few people that use it for their work and were at least inconvenienced by it. I read the report with somewhat the same reasoning that one watches Nascar, to see the big wreck and find out how it happened. But reading these things helps you think about how you could avoid such wrecks in your day job, so it’s useful reading.

The story goes that 30 million computers around the world running Skype all downloaded a Windows Update and did a restart, all at the same time. I always wondered how Microsoft’s servers could keep up with that, but I guess they did very well. But when those 30 million Skype users all tried to log into Skype after their restart all at the same time, bad things started to happen and everyone got booted off the system.

Now, being a software professional, it’s not clear to me how this outage could last two days. Normally, you get a timeout if the server is busy and after some amount of time you retry. You’d think there would be a variability in the timeout so that everyone doesn’t retry all at once, but maybe that was the flaw they found.

But the lesson of the day is to always consider the “impossible” since sooner or later, it may not be impossible. We run into that with the CDT. We find users who take the CDT and import any old project they may have and expect the CDT’s parsers to find everything. In a lot of cases, we’re fine, but we definitely don’t take into consideration all possible scenarios. And I think that will be the next phase of CDT’s lifecycle, to reach that maturity where our feature set does work on more and more projects and we can have more and more happy users added to our community. Openning our minds to the impossible will help us get there.


