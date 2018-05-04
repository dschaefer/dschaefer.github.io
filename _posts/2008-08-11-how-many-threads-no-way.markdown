---
layout: post
title: How many threads? No way!
date: '2008-08-11 11:44:00'
---


Well, I thought I was being sneaky when I googled for the Intel Larrabee paper that is being presented tomorrow at SIGGRAPH and thought you had to be an ACM member to get a copy but then found it on the Intel site. Everyone else seems to have found it too. To save you the hastle, [here it is](http://softwarecommunity.intel.com/UserFiles/en-us/File/larrabee_manycore.pdf). I found the link today on Wikipedia so apparently it’s no longer secret.

Anyway, I’m more curious about it than anything. And I guess the biggest question I had was how many cores the thing is supposed to have. This will help me measure how pressing the need is to figure out how to program many threaded applications without Joe programmer’s head exploding.

Well there’s no actual product announcement in the paper, which I guess is the right thing since it’s a conference paper aimed at getting graphics programmers interested in their architecture. But the performance charts give a hint. They show the number of cores needed to make some of the popular recent games hit 60 frames per second where you generally need between 24 and 32 cores. They then show some charts showing scalability up to 64 cores. Given that, I think it’s safe to say we’ll see 24-32 core Larrabees in the not too distant future and grow from there.

But wait, there’s more. Each core has 4 threads of execution to help ensure that the cores are kept busy while waiting for cache and memory and I/O and stuff. That gives you up 256 concurrent threads in the 64-core monster and 128 in the regular 32-core machine. That’s a lot of threads. And, yes, it’ll be hard to write applications that can get the maximum performance from these.

One other thing I found interesting is that their performance tests were done with the cores running at 1 GHz. That’s pretty slow by modern standards. And it explains why they are focusing on graphics co-processor applications where programmers are already trying to figure out how to make things more parallel. If you don’t, you’re single threaded application running at 1 GHz will be pretty slow (trust me, I have a 667 MHz Pentium III at home, brutal). So until multi-threaded programming becomes more mainstream, don’t expect to see one of these things running your Office suite or Eclipse – even though it could.


