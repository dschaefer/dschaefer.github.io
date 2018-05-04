---
layout: post
title: Tracking Language Trends
date: '2006-05-11 08:58:00'
---


After reading Ian’s post on [Eclipse language support](http://ianskerrett.blogspot.com/2006/05/different-language-support-for-eclipse.html), I had to check out where he got the ranking information. It is provided by [TIOBE Software’s Programming Community Index](http://www.tiobe.com/tpci.htm). I’m sure you can debate the merits of this index and the fact it is based on hits from the top three internet search engines, but as with all polls, it is pretty interesting to look at.

I’m pleased to see that, despite continuous predictions of C and C++’s demise, they still still #2 and #3 in this index, “eclipsed” only by Java. It is also interesting to note that C is still way ahead of C++. This is something we are seeing in the embedded space, where C++ is still seen as too expensive in size and performance for devices. For very small footprints, this is actually true, but the amount of memory and CPU power available in embedded devices continues to grow and this is becoming more a cultural issue than a technical one.

I was surprised to see PHP listed so highly, at #4. I guess I’m still suffering from my brainwashing that [James Gosling did on me](http://mea-bloga.blogspot.com/2006/05/i-declare-shenanigans.html) that Java was the only language for internet applications. The rise of PHP is probably killing Perl, which isn’t surprising as I consider Perl one of those “write-only” languages. I was somewhat disappointed to see the .Net languages so low, but then I’d bet that their query on Basic is picking up VB.Net unintentionally, which if true puts it on par with PHP.

I’ve been a huge fan of programming languages and paradigms since my university days many moons ago, which is probably why I’m so passionate about the CDT and why I keep pushing the CDT to make sure the it can handle multiple languages. To a large extent, we treat C and C++ as separate languages, so adding a new one shouldn’t be that hard. We have Photran team exercising that with Fortran (which failed to make the top 20 but sits at #21, stay tuned for it’s renewed meteoric rise!). I also have a hook on a student in Google’s Summer of Code that is interested in doing C# and VB.Net for Mono.

Being compiled languages, they benefit mainly in the build and debug side of things, but I’m hoping to extend it to the editor and indexing side with CDT’s code models. IDE generation is one thing, but to be fully functional environments for complex industrial strength languages with all the wizbang features of the JDT, you need a solid extensible framework that we are hoping to provide with the CDT. It’s all really cool stuff, well for me anyway, and, of course, helps build the CDT community by expanding it’s horizons.


