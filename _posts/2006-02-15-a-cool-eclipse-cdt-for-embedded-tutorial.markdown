---
layout: post
title: A Cool Eclipse CDT for Embedded Tutorial
date: '2006-02-15 12:06:00'
---


I often hear the remark that the CDT isn’t good for embedded development. I always find that odd since the majority of the contributors and commercial consumers of the CDT are embedded tools vendors and the CDT actually sprouted out from one such tool. Mind you there are a few things that the commercial vendors add to make things like board bring up and target management easier but these aren’t huge additions.

But having been in the tools business for over a decade now, I find it much easier to sell such ideas if there is a grassroots movement that is driven by real users’ needs. That’s when I was thrilled when Wayne Beaton passed on a proposed Eclipse article based on a turorial on that very subject. The tutorial is written by James Lynch who has given me permission to pass it on to you. You can see the [tutorial here](http://www.olimex.com/dev/pdf/ARM%20Cross%20Development%20with%20Eclipse%20version%203.pdf). The objective of it is to show that you can do embedded development on an inexpensive environment for people who want to play and learn about the embedded world. Mission accomplied I’d say!

The tutorial walks the reader through how to set up their Eclipse environment and other tools including a special embedded version of the CDT that our friend Øyvind at Zylin Consulting has put together. He then shows how to code up an small image that strobes an LED on the board and how to build the image, download it using JTAG and debug it over a serial port. It’s a very cool illustration of our point that “Eclipse is not just for Java”.

Now, I’ll need to take a look at the changes that Øyvind has made in his version of the CDT and see why we couldn’t make them available in the base CDT. That would make it even easier for everyone who wants to try it out.


