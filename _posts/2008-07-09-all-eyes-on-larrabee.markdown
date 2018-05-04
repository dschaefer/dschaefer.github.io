---
layout: post
title: All eyes on Larrabee
date: '2008-07-09 13:57:00'
---


There’s been a bit of talk on the web-o-sphere about a [report out of the German tech magazine Hiese.de](http://www.custompc.co.uk/news/602910/rumour-control-larrabee-based-on-32-original-pentium-cores.html) that claimed that the Larrabee multi-core processor that Intel was working on will contain 32 original (well, second generation, but still 20 years old) Pentium cores. In the end, it appears to be just speculation and Intel was quick to squash the rumors. But the logic behind the speculation seems plausible.

The old Pentiums where 3 million transistors and with the new GPUs coming out with over a billion, you pack a lot of cores onto one of those. And I like the concept. Something old is new again. Simplify and multiply. There are a lot of transistors in modern CPUs just to handle out of order execution and try to do as many things at once at the instruction level. But that’s pretty complicated but made it simple for the programmer. We’ve gotten pretty good at doing the simple things, why not just take a step back and use what we know. But, of course, you still need to software to take advantage of it.

Reading the discussions really opened my eyes a bit more. This 32-core thing really is possible and will happen within the next year or so. Are we ready to build software applications that can do 32 things at once in an organized fashion. Thinking about it a bit over my holidays here, there is some existing technology we can use and it’ll be pretty familiar. I’ll blog more about it in a couple of days or so, but think C++, generics, SystemC, UML action semantics. Mix them all in a pot and I think we can come up with some “soup for the multicore programmer’s soul”…


