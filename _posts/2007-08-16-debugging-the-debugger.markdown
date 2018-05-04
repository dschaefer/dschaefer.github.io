---
layout: post
title: Debugging the Debugger
date: '2007-08-16 14:39:00'
---


I’ve been trying out MinGW’s new 4.2.1 gcc compilers. As I [mentioned previously](http://cdtdoug.blogspot.com/2007/08/mingw-gcc-421-now-available.html), they’re experimental. But I’ve gotten really good feedback from people that moving to 4.2.1 is a great move and will help make MinGW a serious choice for developers.

They actually have two variants of gcc that they’re working on. One of them supports exception handling based on the debug information gathered using the [DWARF standard](http://dwarfstd.org/). It’s apparently much more efficient than the default one based on setjmp/longjmp. I’m not sure what that all means, but my take is that the dwarf version is better.

At any rate, I had a problem using the dwarf version that I didn’t have using the default (sjlj) version. If I specify the path to a file using Windows traditional back slashes, e.g. ..\main.cpp, gdb got confused and I couldn’t set a breakpoint on a line. And, unfortunately, CDT’s builder builds files this way and I my breakpoints failed to get set.

So, I downloaded the source to MinGW’s gdb, configure and built it and set up a debug session, all within the CDT (this worked since configure generates forward slashes). I was able to set breakpoints, look at the dwarf symbol data that gdb was trying to use and found where the line number info was missing. And with that information, I was able to generate a hopefully helpful bug report that the MinGW developers can take, or if I find the time, I can try out different solutions. The only trouble I had was making sure which gdb was which :).

At any rate, this brought home again why I love using IDEs for development (which gave me a great intro for an article I’m writing). The productivity of using a debug environment that provides point and click visualization of debug information has to be at least ten-fold over using command line debuggers, and maybe a hundred-fold over using printfs. Once you start using it, you’ll never go back.


