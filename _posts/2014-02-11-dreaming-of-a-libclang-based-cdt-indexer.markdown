---
layout: post
title: Dreaming of a libclang-based CDT indexer
date: '2014-02-11 22:09:11'
tags:
- eclipse
---


There’s an exciting competition happening in the C/C++ compiler area lately. Everyone knows about the GNU gcc compiler. It’s been around for a very long time and is a champion when it comes to generating small object code that runs fast. It’s the heart of every Linux system out there and has the vast majority of the market for almost every embedded system out there. What’s not to love, it’s free, fast, and very good.

But there is one thing. It’s GPL. And that’s OK for tools. There are a lot of tools that are GPL and we’re OK with the license because it’s all stuff we want to share with the community so we all benefit from making it better. GPL helped get open source off the ground by forcing a mindset change from a world where secrecy and intellectual property rights trumped all, even though you were so limited in what you could do in some areas with the small handful of engineers who happen to work for you.

It’s when you start wanting to mix licenses where you start to run into trouble. In the early days of CDT, we had a “architect” drop by and challenge why we were building our own parsers for C and C++. “Why not just leverage gcc’s parser”. Well, dude, you can’t do that without infecting your code with GPL. In the end, as I understand it, that was OK since gcc didn’t really have an API for that anyway.

Many years later, enter LLVM and the Clang C/C++/Objective-C compiler based on it. It’s good and only getting better. It promises fast compile times and, importantly for us, [it has a great API](http://llvm.org/devmtg/2010-11/Gregor-libclang.pdf) that lets you take advantage of its ASTs and index. And it has a [much more liberal BSD-styled license](http://llvm.org/docs/DeveloperPolicy.html#copyright-license-patents) which doesn’t force derived works to carry the license. That lets you build commercial software based on it and carry your own license. And it should be compatible with EPL so we could use it with the CDT. [Here’s an example of someone who’s used it to implement features for Emacs.](http://ffevotte.github.io/clang-tags/)

I’ve known about Clang and it’s library, libclang, for a while and we had a quick discussion on the cdt-dev list about using it. I think we agreed that it could be good, but definitely acknowledge it would be a lot of work. I’ve had a friend of mine doing a contract for us working on the current CDT indexer and every time we run into serious issues with the parser and scalability and just general bugs, I start to wonder if it may be worthwhile in the end to purse a libclang based indexer for CDT. Will it be a net gain in the end, who knows. But I can tell you this: It would be an pretty exciting project for someone who wants to get involved with Eclipse and the CDT.


