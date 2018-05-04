---
layout: post
title: What do you use for UI testing?
date: '2007-02-12 14:12:00'
---


The TPTP gang were adjusting version info in an [enhancement request](https://bugs.eclipse.org/bugs/show_bug.cgi?id=138369) I raised against their [Automated GUI Recorder](http://www.eclipse.org/tptp/test/documents/userguides/Intro-Auto-GUI.html) (AGR) and it reminded me I need to look into this issue again. I remember seeing a demo of the AGR back when I snuck into an Eclipse Architecture Council meeting a year or so ago. It looked pretty good and appeared to do what we’ve needed for the CDT since forever, i.e., something to automate testing the GUI.

The issue I have had with the AGR is that I want to integrate the test cases that AGR generates into our existing JUnit framework. Unfortunately, that was impossible, or more realistically, was a lot of work to do. And, also unfortunately, the word I hear through the grapevine is that the AGR really isn’t staffed well enough to evolve it this significantly. It met the needs it was created for, i.e. test TPTP, and if it is to fulfill a larger role in Eclipse, it really needs more Eclipse developers contributing to it.

So if the need isn’t there to trigger this investment, it got me wondering what people use to automate their GUI testing. Of course there are commercial products out there that do the trick and we’ve used those here at QNX. But for open source development, it would be nice if we had an even playing field so that anyone could contribute tests without having to purchase the “standard” tool, assuming we could even agree on which “standard” tool to use.

I heard of the Abbot GUI tester and the Costello GUI recorder, still the best names in open source IMHO, a number of years ago. While built for Swing/AWT, they started working on SWT support a long time ago but it has been slow going. I have heard of some people using it for their Eclipse testing, but I’d like to see an official release of it before committing to it. But it does what I want, though, i.e. integrate with normal JUnit.

So I’d like to hear people’s opinions on this, especially on where they would like to see developers invest their time if they indeed wanted to contribute to an Eclipse open source GUI testing tool. I think the need is there, but that means “beans” if no one else does.


