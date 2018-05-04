---
layout: post
title: Javascript and C++, eh?
date: '2008-11-28 20:07:00'
---


I can’t get my mind off of Dave Thomas’s keynote at Eclipse Summit Europe. His words made so many things crystallize in my mind. I’ve stated many times before in this blog and in my day job, I hate Java. It’s an incredible irony that I do my day to day coding in Java to support developers who focus so much on efficiency and performance and use C mainly to accomplish that with a sprinkling of C++ for good measure. And then to hear their constant complaints that Eclipse is too slow. My good friends in Java VM land tell me not to blame Java for that, but you know, it’s so tempting.

Dave mentioned that applications should be written in C++ and JavaScript. I dunno. C++ has it’s difficulties, there is no doubt. It’s hard to write good C++ programs. That’s why the mix with JavaScript made me think. Does it make sense to build an application where your hard core performance focused code and code that interfaces with the underlying system is written in C++, but all the code that manages interactions with the user is done in JavaScript?

I’ve started to take a look at [Google’s V8 JavaScript engine](http://code.google.com/p/v8/). As they say in their videos, they’re built for embedding in C++ applications and they have implemented some interesting tricks to get JavaScript to run fast, such as a JIT compiler and some heuristics to make class property access faster. As well, they have an efficient memory management system which includes being able to persist snapshots of the heap, including the JITed code, out to the file system for faster startup.

That got me thinking of Eclipse, of course, or really IDE’s in general. What if you take a cross platform GUI toolkit like [wxWidgets](http://www.wxwidgets.org/), add in a component model to allow for dynamic extensions, plus rewrite the CDT parsers in C++ for speed, plus …, and throw in a JavaScript engine like V8 to make it easy for users to program, wouldn’t that make for an interesting architecture? But we already have Eclipse so why would we do that all again? Just a question…


