---
layout: post
title: More word on massive multicore
date: '2007-06-14 15:30:00'
---


I was just reading [this article](http://news.zdnet.com/2100-9584_22-6190856.html) on Intel’s work on trying to bring massive multi-core processors to market. The had showed a demo back in February [that I blogged](http://cdtdoug.blogspot.com/2007/02/now-what-am-i-supposed-to-do-with-80.html) about back then. However that chip didn’t really do anything other than run 80 threads at a time. It didn’t have I/O or memory from what I could tell.

So now the press is trying to figure out how Intel will productize that. I think the article asks some pretty irrelevant questions, like “Will they be x86 cores? Will they run today’s applications?” And the response is that they are working on it to make it easier for programmers to deal with.

But I think that’s a mistake. Why would you run your favorite e-mail program on an 80 core machine? Eclipse, now that I can see, especially if you’ve ever debugged a run-time workbench and saw 30+ worker threads going at it. But really all we’re doing there is taking the same old paradigm and stretching it beyond it’s limits. The hardest bugs I’ve had to solve were when multiple threads were contending for the same resource and someone forgot to synchronize them. Happens time and time again.

No, 80 cores are great. Mix that with 128 stream processors like those on the latest GPUs, and there’s some massive horsepower that we can take advantage of. You can hide all the complexity behind good compilers and run-times, but I don’t think you’ll get all the benefits of the hardware. I continue to believe that we need some new programming paradigm where we stop thinking of programs as a sequence of operations and more like a network of data flows. Turning to objects was the first step, but I think there’s further we can go.


