---
layout: post
title: Oh, I hate Cygwin
date: '2007-04-12 09:40:00'
---


I usually try not to blog while I’m angry. But I’m in the middle of trying to get the [Firefox source](http://www.mozilla.org/developer/) set up in the CDT on my laptop, which, of course, is running Windows (XP mind you, still not brave enough to try Vista). And it has been a struggle.

First of all, it was a bit tricky to set up the build environment. I’m using [Cygwin](http://www.cygwin.com/) since Firefox would really rather be built on Linux, or in a convoluted environment that involves using Cygwin but the Microsoft tool chain, which the CDT doesn’t really have support for yet. Luckily I found a [web page](http://citations.mozdev.org/mozilla-build-win32.html) that showed how to set it up to use the cygwin compilers. It’s a little out of date but a few tweaks and I was able to get Firefox built.

Now I’m trying to get the build output into the CDT so that our cool Scanner Discovery feature can parse it and set up the include paths and symbols for the indexer. That’s been tricky since the Firefox build wrapped all calls to gcc with a wrapper script which deals with converting paths, I guess. I’ve got that fixed, but now the source file paths used by Firefox uses the cygwin paths, i.e. /cygdrive/…, which our build output parser doesn’t understand. So I’ll have to introduce a new parser that does the cygpath conversion.

We’ve had a lot of bug reports lately on cygwin. Most of them have to do with the cygwin developers deciding not to support Windows path names any more, you know, the good ol’ C:\blah. I guess understand their reasoning. Cygwin is meant to be a Linux emulation environment on Windows. I don’t think that was their original intention since Cygwin actually predates all this Linux popularity, but that’s what it has turned into (and even their [web site](http://www.cygwin.com/) now says so).

The issue for the CDT is that it isn’t running under the cygwin environment. It can only deal with Windows paths. So whenever we see a cygwin path, we need to convert it. Not only that, when generating makefiles for cygwin make, we need to convert Windows paths to cygwin paths. Now, we can’t do that for everything on Windows since tools like MinGW gcc does use Windows paths. It’s pure evil (well maybe not that evil…)

So what this really means is that supporting Cygwin with the CDT is becoming a lot of work. This is one of the reasons I want to start promoting [MinGW](http://www.mingw.org/), a much more Windows friendly port of the gnu tool chain, as the gnu environment of choice on Windows. The problem, though, is that cygwin is very popular and easier to install and seems to have much more momentum than mingw. So we will need to continue to support both. But I’d sure like to see more of that momentum shift to MinGW. Which, in open source, that means I need to do more to help them.


