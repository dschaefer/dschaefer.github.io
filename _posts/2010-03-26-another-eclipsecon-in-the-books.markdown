---
layout: post
title: Another EclipseCon in the Books
date: '2010-03-26 00:05:00'
---


Wow, what a week. I don’t even know where to start. There were a lot of old familiar faces here, there were a lot of new people who introduced themselves to me. The CDT community is thriving and I am more excited about CDT’s future now than I ever have been.

The main reason for that I think is that we’re starting to go beyond our basic set of features into some things you won’t see in most IDEs. The big one for me that only made a little splash is CDT’s new Codan static analysis framework and it’s current small set of checkers. Today, CDT will detect syntax errors and highlight them. But with Codan, we can now detect logic errors. Things that have traditionally made C development hard, like finding unbalanced malloc and free’s, or new’s and delete’s, that lead to memory leaks, can now be checked for with the appropriate checker. It’s pretty new and will only be available for preview in CDT 7.0, but I can’t wait to see where the community takes this.

The other big activity in CDT is our new built-in debugger that gives us the ability to debug without having to rely on an external debugger. It’s also in a preview state, but companies with special debug needs that aren’t being met by gdb, have an opportunity to use a debugger much more tightly integrated into Eclipse, and fully licensed EPL. And no, we’re not planning on a EPL compiler, just dreaming of one :).

I am also seeing things happening on the periphery of CDT that extend Eclipse’s C/C++ development beyond our traditional edit/build/debug. Tracing and profiling are maturing. Support for a “best in class” Linux IDE. Debugging for massive multi-core. It’s as though we’ve now solved the basics and are now focusing on the hard problems, and doing it in the open. It’ll be very interesting to see where things go and how we manage the community to make sure we’re efficient.

Along with parallel tools and Linux communities, I’m getting more involved with the Mobile projects. It’s part of my role as an Architecture Council mentor to help them out. But I think there will be some overlap between Mobile and the traditional embedded that the CDT community represents. There was some great discussions this week in that area and I’m happy with the progress they’re making.

But it’s time to go home and back to the grind. The CDT community and the communities it intersects with are thriving and I can’t wait to see where we end up by next year’s EclipseCon, same time, same place, in 2011.


