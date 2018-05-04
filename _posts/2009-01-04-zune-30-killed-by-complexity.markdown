---
layout: post
title: Zune 30, Killed by Complexity
date: '2009-01-04 20:27:00'
---


I first heard of it early New Years Eve, I guess. Hoards of Microsoft Zunes were [committing mass suicide](http://it.slashdot.org/article.pl?sid=08/12/31/1428254) (a gruesome thought but the actual quote from the Slashdot article). Fears rose that some Y2K thing was happening, mind you things like that didn’t happen in Y2K, at least not on this scale. [Microsoft finally confirmed](http://www.zune.net/en-us/support/zune30.htm) the issue as such though, a device driver hang on the 366’th day of a leap year. I’d love to see that code…

Well, thanks to the wonders of the internet, [here it is](http://pastie.org/349916)! (I imagine this link will fall dead as soon as the Microsoft cronies make the rounds, as they should. It does have a Microsoft copyright). I actually found it through another blog where the guy put together a [pretty good analysis of the problem](http://www.aeroxp.org/2009/01/lesson-on-infinite-loops/).

The root cause? A brain fart. Either someone was in a hurry, or they couldn’t handle the complexity of the algorithm once they started dealing with leap years. People blame testing for not testing all the paths. But, if you don’t take the time to test all the paths, or don’t have the skills to properly enumerate all the paths, testing isn’t going to matter. At any rate, another great software engineering lesson learned for us all, just like the [unhandled exception in the Ariane-5 rocket](http://en.wikipedia.org/wiki/Ariane_5#Launch_history), except this one is recoverable and isn’t as expensive (unless the Zune market share dives as a result, which could happen).

I spend a lot of my time these days working on software architectures and trying to come up with the most simple, extensible, and future proof. But none of that matters if you have code like this. And I’ve seen code like this all through my career. Hell, I’ve written some of it. But one thing I learned early from [one of my great profs](http://www.cs.usask.ca/faculty/tremblay/) back at the [U of S](http://www.usask.ca/), was on code complexity. [It is even measurable](http://en.wikipedia.org/wiki/Cyclomatic_complexity) by counting the number of paths through your code. Complexity bad. Which implies that having more paths than you need is bad. As we see here, it becomes too difficult to test fully.

And that is certainly the case here. Too many ‘if’s. How do you convert days since 1980 into a time structure? Well in the Zune code (which is actually a common device driver in a number of Windows CE platforms), one of the paths leads to an infinite loop, when days is 366 and IsLeapYear is true. The author of the blog proposes a much simpler algorithm that works correctly but reduces the paths thus eliminating the bad one. I think you can make it even simpler.

One of my mantras is “I hate typing!”. Of course it has nothing to do with typing (much). It’s about producing simple elegant solutions to simple problems. Yes, Keep it Simple S(favorite ending here). Saves time. Saves money. Saves embarrassment. Saves your job. I’d hate to be the guy who wrote this code…


