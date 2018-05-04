---
layout: post
title: exit() is your friend
date: '2008-09-03 13:16:00'
---


I was just reading the [Google Chrome cartoon book](http://www.google.com/googlebooks/chrome) (an interesting way of presenting designs). One of the things they talked about was how having browser tabs in separate process helps with memory consumption because memory gets cleaned up with the process exits. Otherwise, the constant malloc/free cycle ends up with memory fragmentation that is hard to get rid of.

That brought back some memories. In my early work on a code generator, I used the same philosophy. I created a pretty big object model in memory after I parsed the input, but I never implemented any of the destructors and never called delete. Didn’t need to. It was a short lived process and the call to exit() at the end freed up all the memory anyway. And it’s pretty fast! Lot faster than calling delete for each object I created.

Anyway that worked great. Until another team decided they liked my object model and wanted to use it in the main tool. Unfortunately that tool was a long running process and they had to add in the memory management to survive. So much for exit() is your friend. Worked for me, though.

Of course all the garbage collector languages deal with this for you. Makes me wonder why GC in C++ hasn’t become more popular. There are C++ garbage collectors like [the one from Hans Boehm](http://www.hpl.hp.com/personal/Hans_Boehm/gc/). But I guess if you’re moving to that paradigm, you might as well use Java.


