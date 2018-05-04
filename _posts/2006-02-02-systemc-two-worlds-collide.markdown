---
layout: post
title: SystemC - two worlds collide
date: '2006-02-02 11:42:00'
---


I used to sit across the cubicle wall from an ASIC designer back in the mid 90’s. He was pretty friendly and was very interested in the future of software engineering, especially software modeling. I guess that makes sense since, as an ASIC designer, modeling hardware was second nature and he figured it should be the same for software.

That got me interested in what they were using to model hardware. He was using Verilog, one of the big two hardware description languages, VHDL being the other. I was starting to use ObjecTime, a graphical software modeling tool that I ended up helping build, and he found it very odd that we were moving into graphical modeling where the hardware guys were abandoning it for textual modeling.

Looking back now, I’m thinking he may have been on to something. I still think visual modeling has a long way to go before it becomes mainstream with every day developers, and even longer for modeling behavior. Maybe we’re suckers for punishment and prefer to deal with reams of text, or maybe the tools aren’t up to snuff yet for visual modeling (and I’m still holding out hope that GMF will get us much closer).

That’s when I ran across SystemC yesterday, I had a famous Ward Cunningham “a-ha moment”. Here’s a system description language that software guys would love. It uses the power of C++’s type system and a small run-time to model the concurrency and timing of real-world systems. What a great mix of the two worlds with hardware and software guys working on the same code. I am just starting to scratch the surface of the potential of SystemC, but it’s one of those technologies that I end up losing sleep over wondering about the possibilities. I’ll write more on it once I do a bit more research and I’d love to hear peoples’ opinions on it.

However, the important thing I am taking from SystemC has nothing to do with systems modeling. At the back of my mind is a new programming paradigm that was sparked when I first looked at UML action semantics. Hardware is inherently a huge collection of concurrent processes, which BTW is also a key feature that SystemC emulates. This concurrency is the reason why many algorithms are much faster to implement in hardware. Why can’t software be that way? And with the new revolution of multi-core processing, will our current von Neumann paradigm scale to hundreds of concurrent threads? Maybe there’s something we can take away from SystemC that we can use to build massively concurrent programs in C++. I sense another “a-ha moment” coming, or at least another few more late nights…


