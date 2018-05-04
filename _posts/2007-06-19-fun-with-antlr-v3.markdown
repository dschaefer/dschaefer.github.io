---
layout: post
title: Fun with ANTLR v3
date: '2007-06-19 09:23:00'
---


A colleague of mine puts it best, “I have a habit of chasing shiny objects”. I’m interested in so many things in this industry that I love to tinker with that I never actually get to finish any of them, other than a C++ parser I once dreamed of :).

The latest shiny object is the new [ANTLR version 3](http://www.antlr.org/), a fancy new parser generator. I’ve followed ANTLR with interest for a few years and we almost used it for CDT’s parser back in the 1.x days. But at the time we felt that hand coding was the only way we could successfully deal with C++ ambiguous statements (e.g. x * y, is that expression, or a declaration of a pointer to x).

The new version comes with an LL(*) parsing mechanism that uses infinite lookahead (the *) to decide what rules a sentence matches. If you aren’t familiar with what all that means, Terence Parr, the author of ANTLR, has written a great book that explains it all for you. The book itself is interesting since right now there is very little documentation other than the book. But it’s only $24 dollars for the “non-dead tree” PDF version and is an interesting way to help fund the work.

But, this is essentially how Johnny C and I wrote the CDT parsers. We start at the high level concepts and break them down into finer grained detail until you get to the individual characters, creating an Abstract Syntax Tree (AST) along the way. You can base interpretation choices on where you are in the analysis and by looking ahead into the source stream as much as you need. It’s a very powerful technique.

With ANTLR, however, you can specify the grammar at a higher level and have it generate a lot of boilerplate code for you. It may be the one parser generator tool that can convince me that it’s better than hand coding. But to figure this out, I decided to try building a parser. Mike and the CDT guys at IBM are already working on a C parser using [LPG](http://sourceforge.net/projects/lpg/), an LR parser generator (LR is bottom up, which, while faster, doesn’t allow you to easily use context information when resolving rules, I prefer LL) and extending it for UPC, [Unified Parallel C](http://upc.gwu.edu/). And since I need to resolve some extensibility issues for GNU versus MSVC, and having a lot of experience in the past, I decided to try a C++ parser.

Now if ANTLR can handle that, I’m sold. It’ll be an interesting journey and should allow me to try out some ideas on improving how we did some of the things in CDT’s parser. Also this is just a prototype and I don’t really plan on replacing CDT’s parser with it. But it will help me learn ANTLR more and help me help others in the Eclipse community who want to use it. And who knows, another shiny object may fly by and take me on a totally different tangent anyway…


