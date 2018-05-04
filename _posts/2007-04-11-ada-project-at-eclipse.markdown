---
layout: post
title: Ada Project at Eclipse
date: '2007-04-11 10:41:00'
---


In all the excitement of the conferences I’ve been to in the last couple of months, I’ve also been helping [Aonix](http://www.aonix.com/) with their proposed [Ada project at Eclipse](http://www.eclipse.org/proposals/adt/), called ADT (of course). Ada, you say!?!?! Yes, Ada. Despite reports to the contrary, Ada is still being used in the industry, especially in the military and aerospace and especially in safety critical systems. And with the introduction of [Ada 2005](http://www.adaic.com/standards/ada05.html), the hope is to spread all that Ada goodness to the rest of the embedded industry.

So, why Ada? Funny enough, googling “Why Ada” returns a number of articles on that subject. This is something the Ada community has struggled with for quite a while. But from my point of view, it all comes down to writing safe code. Ada is a huge language and much of it has to do with making as hard as possible to write bad code. Code like “while (i++) *i = 42;” isn’t possible. This is particularly of importance with embedded systems where flaws like this could be costly, very costly.

But Ada has also suffered from the stigma of bureaucracy. The fact that it was designed by committee for the U.S. Department of Defense (who has since dropped it as a requirement) doesn’t help. Also the reference manual reads like a legal document, and there are few books out there to explain it to us regular Joe’s.

From my perspective, though, I think the biggest problem with Ada has been the lack of an open source community around it. [GNAT](http://www.gnu.org/software/gnat/gnat.html), the GNU Ada compiler has been around a while, but it isn’t very straighforward to use with it’s own build system. But gdb works fine with it for debug.

So, in the past, I’ve tried to drum up interest in Ada as an extension of the CDT at Eclipse. Aonix and [AdaCore](http://www.adacore.com/2007/04/03/adacore-announces-gnatbench-version-20-for-eclipse-32/) are two vendors that have done it commercially. I was thrilled when Aonix approached me about starting up such a project. And I really hope that other Ada tool vendors join in on the fun.

High quality open source solutions available to everyone really helps with growth at the grassroots level. Many universities and colleges are using the CDT for their coursework because it is freely available. The same could happen with the Eclipse ADT. But to ensure high quality, a community has to form around it to share in the work. Most Eclipse projects benefit from the spirit of “co-opetition”, competitors working together for the common good of the market. This could grow the Ada market which would mean they could sell more professional tools and support. Such is the economic wheel that keeps Eclipse going and we’ll see if the Ada market can do the same.


