---
layout: post
title: Mobile will drive &quot;IDE in the Cloud&quot;
date: '2009-07-16 20:21:00'
---


I’m in the middle of making some last minute code changes for work before I start my vacation, or staycation as I hear lots of people calling it these days. We have a pretty big JUnit regression suite to test our p2-based installer, and I made the mistake earlier this week of not running it and ended up having to rewrite the algorithm to solve scalability issues. Lesson of the day, don’t create too many Java objects in long running native code, Lord knows when they get garbage collected.

**This mobile machine’s hot, man!**

The main reason I didn’t run them was because I was working at home with my laptop that day. These long running tests create some massive heat build up in my machine. I lost a hard drive a few years ago doing something like that and it’s made me nervous ever since. I really don’t think laptops are built to handle the intensive compute and disk workloads that I need as a software developer. I think I’m pushing the envelope too far. In fact, I was going to start this blog while the tests were running earlier this evening but the heat knocked out my wireless.

**The ultimate mobile developer platform?**

I’m sure you’ve all been following the Chrome OS “shiny object of the week”. The technical details of the OS itself and the supposedly sinister plot by Google behind it aside, there is no doubting that the designs for the upcoming sub-netbook, aka smartbook, machines are pretty exciting. All day battery life, integrated 3G or WiMAX connectivity anywhere, and with big enough screens to actually be useful. And, yeah, looking at the processors that allow you to do that, you aren’t running Eclipse and gcc on these things to any great scale. But I’d love to use one of these things around the house or on trips to write code with. Especially if it lets these burn marks on my legs heal 😉

**Mobile will drive IDE in the Cloud**

So assuming you want to write software using a mobile device, how would you do it? And, you know, after all the naysaying I did about “IDE in the Cloud” at EcilpseCon, I finally get it. Wouldn’t it make sense to have a workstation setup where you keep all your development tools and do your builds and run your tests, and then be able to access that all from a web browser anywhere in the world? from any mobile device in the world?

That flexibility will drive demand for this architecture, for similar reasons we used this architecture in the pre 1990’s where we used to have dumb terminals connected to powerful DEC VAXen (at least they were powerful for the time). What we’re talking about isn’t much different than that, only the terminals, i.e. the mobile devices, are a bit smarter. But then the compute servers are probably equivalently faster if not more so.

**An opportunity to simplify**

And, yes, we do use VNC and other remote desktop protocols and clients to accomplish this today. And maybe you can so something similar in a browser (in fact I know you can, ever see WebHuddle?). But with these things I think you’ll run into the screen size issue. Myself and a lot of my Eclipse community colleagues have presented Eclipse on 1024×768 projectors and it’s brutal. The IDE just doesn’t scale that small to be useful. But this is the screen sizes you have to deal with on mobile devices.

While working through this new architecture and solving that problem, I think it’s also a great opportunity to simplify the IDE. New users find Eclipse overwhelming with all the views and toolbar buttons and menus, it’s really tough to know what to do next once you fire it up. Being in a browser opens the door to new ways of working. I think we’re still trying to figure out how to do content creation via a browser, and from Google Apps and Microsoft’s upcoming web-based Office suite, we’ll learn a lot and maybe some of these things can be applied to software development.

**Is it time for a new platform?**

Mobile is driving a lot of change in the software and device world. I really believe the software developer will be able to benefit from it. But I wonder whether the platform we’ve built with Eclipse is the right vehicle for this. I know the IBM team is scrambling with e4 to address that. But I’d like to see real innovation here, something that breaks away from the old desktop IDE paradigms of the past. Maybe Eclipse’s “Black Swan” is out there. If it is, we’ll have to make sure we recognize it and welcome it to the community.


