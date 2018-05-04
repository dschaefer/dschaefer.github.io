---
layout: post
title: gdb is a-calling
date: '2007-05-13 22:31:00'
---


I’ve been working over the past week trying to get process interrupts working on Windows so that we can get suspend working again with gdb. The suspend call gets translated to a SIGINT signal raised on the process, which on Windows gets converted into a Control C event. For some reason it stopped working lately, mind you I don’t remember ever actually trying it. It was fun, though. It got me back to my roots as a Windows developer and renewed my dislike for [Hungarian notation](http://en.wikipedia.org/wiki/Hungarian_notation).

Now that I got it working, though. I am finding that when you suspend gdb, both the cygwin version and the mingw version, that you end up in a pretty useless state. The stack trace has gdb totally confused. The addresses don’t even look like real addresses. I thought for a moment that it was because of something I did in the CDT. But when I tried it from the command-line I got the same result. I did a Google search and looked at the cygwin and mingw forums and couldn’t find anything useful. Maybe no one cares. Maybe it’s my machine. Who knows (do you?).

At any rate, it has led me down a path to take a deeper look at how gdb is implemented and try and debug it myself. This is something that I’ve wanted to do for a while. We use gdb as our debugger in QNX Momentics so I may be able to help out our gdb guys too. It’ll also give me something else to test the CDT with. I’m not sure we’ve tested Makefile projects enough in CDT 4 so this will give me a chance to do that. My focus will be on MinGW gdb and it would be cool to be able to contribute any fixes I come up with, or even a port to the latest gdb back to these guys.


