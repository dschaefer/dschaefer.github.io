---
layout: post
title: Are you ready for 1000 cores?
date: '2008-07-02 15:52:00'
---


Massively parallel computing is something I’ve been interested in for a while and have blogged about a few times in the past. [This blog entry by an Intel Researcher](http://blogs.intel.com/research/2008/06/unwelcome_advice.php) made me think about it again. He continues to proclaim that the future isn’t that far away and we had better start designing our software so that it can run on machines with thousands of cores. He worries that we’re aren’t ready yet and we need to start getting ready. And he’s right.

Being a tools guy, I think this is the next big paradigm that the tooling industry needs to address. Object-oriented programming and design was a godsend when machines started scaling up in the size of memory and storage and our programs began filling that with data. We built a lot of tools to help with that. Programming languages and compilers are obvious examples. But so is the JDT and CDT, with their code analysis to show type hierarchies and help you easily find classes. Not to mention all the object modeling tools for drawing pictures of your classes.

Coming up with the languages and compilers and other tools necessary to deal with thousands of concurrently running threads is our next great challenge. This is why I keep one eye on the [Parallel Tools Project at Eclipse](http://www.eclipse.org/ptp/). They’re already in this world dealing with the thousands of processors that run the super computers they work with. This effort is a research project in itself (quite literally if you notice who participates in this project :).

But as the Intel researcher warns, this stuff is going to hit the mainstream soon. We’re starting to see that with [OpenMP parallel language extensions](http://openmp.org/wp/) supported in almost all recent compiler releases, including gcc. And I’m convinced it’s an area where modeling can help since you really need to think of your program in multiple dimensions, which is something modeling is good at.

I think it’s a matter of time before we’re at the head of a new paradigm. I remember the fun we had when object-oriented programming hit the mainstream. I think this one will be just as fun.


