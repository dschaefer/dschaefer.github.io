---
layout: post
title: CDT 5.0 for Ganymede, Come get Some
date: '2008-06-25 10:52:00'
---


CDT 5.0 is out the door and available at your friendly Ganymede update site. I’m sure the Eclipse servers will be busy the next few days. The Eclipse community is vast and they love trying out the shiny new features that we’ve worked hard on all year to make.

I’m especially proud this year with CDT 5.0. With my new job at Wind River working on a p2 based installer, I’ve finally have a real reason to use it to write the JNI code that I need for some of the computation intensive parts of it. BTW, I now have proof that the Java version of an algorithm is much, much more compute intensive than a C version, check out the LZMA SDK from 7-Zip.

I’m really enjoying the experience. When I first imported the LZMA SDK into my C project, the first thing I needed to find out was where the main() function was. Let’s try the Open Element dialog (Shift-Ctrl-T), typed in main, and there it was! A couple of Open Declarations (F3) later, and I was able to find the implementation of the decode function I needed to use. Awesome and I didn’t even notice the Indexer running to find all this stuff. And everything else looked clean and worked well.

So yeah, the JDT guys are probably laughing since they’ve had all that stuff working well for a few years now. JDT has always been our bar (along with VisualStudio which I think we reached a while ago). But watch out. We may just make the CDT so good that people will wonder what the hype about Java was all about 🙂


