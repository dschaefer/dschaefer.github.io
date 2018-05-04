---
layout: post
title: Common Navigator misses the mark
date: '2009-05-23 18:53:00'
---


What’s wrong with this picture:

[![](http://1.bp.blogspot.com/_X6Gz24BqUwI/ShiMruX4d1I/AAAAAAAAAA4/wU6ejeZj8Q4/s400/NavigatorProb.png)](http://1.bp.blogspot.com/_X6Gz24BqUwI/ShiMruX4d1I/AAAAAAAAAA4/wU6ejeZj8Q4/s1600-h/NavigatorProb.png)

This is a Android project that includes both JDT and CDT natures to build an Android app with a native library using the upcoming Android Native Development Kit. As you can see both JDT and CDT contribute to the list of things in the project. The Resource system would put it’s own twist on the project if I hadn’t turned it off.

The Common Navigator was a great idea when it was proposed. Have a single navigator framework that projects could contribute to. I have the sense it wasn’t meant to handle the use case where you’d want to see a project that that has multiple natures leading to multiple contributors. The result is confusing at best, and embarrassing at the least.

But it’s a good example of where the Eclipse dream of interoperability is a bit of a failure. Yes, there is a bug on this (didn’t have time to look up the number but one of the CDT committers warned that this was going to happen). And my understanding is that it won’t make the cut for 3.5 meaning this behaviour will be seen in commercial products as well, unless the vendors fork and fix it locally. And it’s just not the JDT’s fault, CDT is helping here too, and not knowing, I wonder if it’s something missing from the framework to help co-ordinate this.

It’s pretty disappointing and, yes, embarrassing, as I try to get the Android community to use the CDT for this style of application. There’s no reason to create separate projects for Java and C++. Everything else is working fine in the one project. They’ll just have to make sure the expand the right version of the src folder to find their Java source, at least there’s icons that differentiate it, unlike the assets and res folders.


