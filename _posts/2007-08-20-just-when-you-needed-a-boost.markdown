---
layout: post
title: Just when you needed a Boost
date: '2007-08-20 10:32:00'
---


I’ve been aware of the [Boost C++ library](http://www.boost.org/) for quite a while, but in the context I had to deal with it, it was painful. The Boost library is a collection of C++ templates intended as a trial ground for additions to the Standard Template Library that is part of the C++ standard. Some of them [according to Bjarne](http://cdtdoug.blogspot.com/2007/08/master-speaks-bjarnes-vision-of-future.html), have made it into the next standard C++0x. But they stretch C++ templates to the limits, and as such, stretched the CDT’s C++ parser to it’s limits and broke it. In the early days of the CDT, we eventually just skipped it.

But lately, Markus on the CDT team has been testing his indexer work with Boost, and I’ve had a number of requests from people to include it in [Wascana](http://wascana.sourceforge.net/). So I decided to take a fresh new look at it.

Now I was expecting some simple container templates and utilities and such. And there were things that are much needed like a threads package for multi-threading your app and a regular expression utility class.

But I was amazed at some of the big constructs they have there. The first thing I ran into is a complete lexer/parser subsystem including a preprocessor. With that, it wouldn’t take to long to build parsers in C++, and maybe even a C++ parser.

As well, there is a Statechart engine. This is something I’ve dealt with a lot in my past and it was cool to see a solution that involved templates and States as objects and some of the neat tricks it used to implement action code. Whether it scales to real size state machines, I’d have to dig deeper to see.

I’ve always been amazed at how powerful C++ templates can be and how the compilers can take all this template code and specializations and such and optimize it down to some pretty efficient code that you probably would have written by hand. But with templates, you work at a higher level of abstraction, meaning higher productivity. Boost gives you some pretty powerful abstractions. We’ll see how easy they are to use in practice.


