---
layout: post
title: How slow is Java? Not as much as you may think.
date: '2008-01-21 13:29:00'
---


I was reading an article on the D programming language (more on that in an upcoming post). At the end of it, the guy claimed it was close in performance to C++. And he used [this benchmarking site as evidence](http://shootout.alioth.debian.org/gp4sandbox/benchmark.php?test=all&lang=all). It measures a number of different programming languages on a couple of x86 platforms at performing various algorithms. Most of the algorithms are pretty intense, so it’s a good measure of the raw compute power of their runtimes.

Now any such measure is easy to dispute. Did the programmers have sufficient knowledge in the languages to build implementations that would be efficient? They do allow you to play with different weightings for different factors that may be important to you. But the results are interesting non-the-less.

So, a couple of things caught my eye with the default results. First, C++ is faster than C. That I can see if you use C++ inlining a lot which is not always easy to do in C. But it is only slightly faster so I’d call it a draw.

Second, if you preallocate 64MB of heap (-Xms), which we often do, Java is only 1.7 times slower than C++. I think that is a very important result. We often wondered if the CDT’s parsers were slow because they were written in Java. The IBM J9 guys said that was crazy talk and these numbers somewhat show their point. Well written Java that really benefits from JIT should be less than 2 times slower than C++. We were looking for a 10 times performance improvement and would probably have been disappointed if we had rewritten everything in C++ (and I mean disappointed in the career limiting aspects of that decision ;).

I don’t know whether to fully trust the numbers on this site, but it does reaffirm my belief that Java isn’t that much slower than C++. I still don’t like Java, though. Show me something as powerful as the Standard Template Library in Java and I might change my mind. Or the ‘foreach’ from D…


