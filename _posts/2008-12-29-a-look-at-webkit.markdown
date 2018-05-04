---
layout: post
title: A look at WebKit
date: '2008-12-29 02:38:00'
---


A few days ago, I was playing with [Google’s V8 JavaScript VM](http://code.google.com/p/v8/) library and got it compiling with [MinGW in Wascana](http://wascana.sf.net/). I submitted the patch to make it work but I haven’t heard back. I guess it could be the Christmas break.

But one thing that struck me odd recently [was an announcement](http://androidgate.com/tag/squirrelfish-javascript-engine/) that the next rev of Android would include [WebKit’s SquirrelFish Javascript VM](http://webkit.org/blog/189/announcing-squirrelfish/). I guess that shouldn’t be too surprising since SquirrelFish comes with Webkit. But then why is there ARM support (the CPU for Android) in V8? And if they are using SquirrelFish for Android, why don’t they use the souped up [SquirrelFish Extreme](http://webkit.org/blog/214/introducing-squirrelfish-extreme/) for Chrome? Especially since there are benchmarks showing it beating V8. I’m confused and can only chalk it up to Google being a big company and maybe the Android people don’t hang out with the Chrome people.

Anyway, that got me looking into this [whole WebKit business](http://www.webkit.org/). I downloaded the latest nightly source build to my Debian Linux VM and after installing a boat load of packages needed to build it, I built it. I had heard the JavaScriptCore library which implements the VM was embeddable in C++ apps. The header files are there, but it looks like you actually have to embed the whole WebKit library to get at the VM.

That got me thinking back to an earlier idea I had. Use HTML with JavaScript as your main GUI framework. With Webkit, you can embed the whole browser into your application, and you can hook up new JavaScript classes to your C++ classes to provide scripting and to give access to them to the UI. Interesting to see how that would work in action.

I think I’m starting to figure out this whole JavaScript and C++ thing, with thanks partly to something a commenter said on a previous entry. Use scripting for quick turnaround, when you want to whip up a prototype or allow for easy extension of functionality. But use C++ for areas where you need to engineer functionality. Part of your architecture design is deciding what that means. And maybe something like WebKit might be the right platform to get you off the ground.


