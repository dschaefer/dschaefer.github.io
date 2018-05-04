---
layout: post
title: Code like you won't be there tomorrow
date: '2008-02-21 10:43:00'
---


One of the things that we deal with on most software projects that continue on for a few years is turnover. People come and go. I’m not sure it’s more prevalent with the software industry than others, but it is painful. As managers we spend a lot of effort making sure transition plans are put in place when it happens so that the asset that is the developer’s knowledge isn’t lost.

Unfortunately, we haven’t done a good job of that with the CDT. We have a number of instances now where developers work hard and put in a great complex framework to solve a really complicated problem. We really appreciate the contributions to make the CDT better.

But stuff happens. The developer gets put on other projects or leaves the company that was paying him to work on the CDT, and poof, the detailed knowledge of what they were working on is gone. But since we don’t really have a manager/employee relationship with them, it doesn’t really cross our mind that we need to manage the transition and make sure we capture that knowledge. And maybe we should.

The other side of the coin, though, is that developers love what they do and want to do it forever, especially on exciting projects like the CDT that are doing good for the world (or something). I’m not sure they consider the possibility that they may get pulled off the project and they don’t spend the time to properly document what they are doing so others can pick up the pieces. Or worse, they try to be very clever in their solution making it more complicated than maybe it could be, and certainly difficult for downstream maintainers to understand.

The concern I often hear from them is that, since it’s open source, their employers don’t give them enough time to do everything you would on a commercial project. And we were also going through a phase where we needed contributions badly and didn’t consider it prudent to enforce that documentation be provided. But we’re definitely paying for it now as we have a pretty big bulk of undocumented code that we’re trying to fix bugs in.

So the lesson of the day is to code like you won’t be there tomorrow. You can create the best system ever, and people will appreciate it while you’re there, but they may end up cursing you if you disappear and leave it in their laps. At the very least, they’ll be wishing you could come back.


