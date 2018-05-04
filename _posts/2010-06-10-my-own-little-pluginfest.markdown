---
layout: post
title: My own little PluginFest
date: '2010-06-10 14:40:00'
---


This is a bit of a follow up to [a blog entry done by my product manager partner in crime here at Wind River, Emeka](http://blogs.windriver.com/nwafor/2010/06/workbench-and-jazz.html). I spent a couple of weeks recently (in the middle of the Helios rush too) to put together a demo he is giving today at IBM’s Innovate Conference. It was great because it reminded us of what we’re really trying to do here creating IDEs using Eclipse, *Integrating* tools.

The the code in the demo is quite small but that’s a good thing thanks to good APIs. It’s a menu item associated with the editor for Wind River Workbench’s Memory Analysis database. The item takes that database and zips it up and attaches it to a newly created Work Item from IBM’s Rational Team Concert, i.e. Jazz, product. The story goes that you see a problem in the memory analysis and you want to record it for someone to look at later. And that person takes the attached zip and opens it up in the editor to start his investigation, using the other information recorded in the work item and documenting his findings there as well.

The value of the integration becomes greater than the combined value of tools that Wind River and IBM have built on their own. And that’s the promise of Eclipse and it was great to see that promise in action. But it also brought home that we don’t see that happening enough. As we solidify the platform and the first layer of tooling, we need to keep driving the solutions and build up a bigger and better stack and sell our collective customers on the value of Eclipse and the solutions we’re building for them.

A few years ago we held a PluginFest where we brought together a number of embedded tooling vendors and tried to plug and play their products. In the end, it was more to test that they co-existed with each other than anything. A few had real integrations to show. But I think we fell short of the goal and dropped the ball on the potential. Maybe it’s time to bring us back together, not to test interoperability, but to explore opportunities to build real value add integrations that we can work on together. Emeka and I and the IBM RTC gang have started down that path. Hopefully it can be used as an example of the real value of Eclipse as an IDE and rejuvenate the ecosystem a bit.


