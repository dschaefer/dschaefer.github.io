---
layout: post
title: CDT in Action on Big Projects
date: '2006-05-02 09:30:00'
---


It’s pretty common [knowledge](http://www.eclipsecon.org/2006/Sub.do?id=76) now that I use the Mozilla, and lately Firefox in particular, as my main test bed for scalability testing. It’s a pretty big project and I have often found issues with the CDT in this environment and we are trying to address them as we can.

I was pleasently suprised the other day when by friend John Camelon (Mr. CDT Parser) brought the following [article](http://developer.mozilla.org/en/docs/Eclipse) to my attention. It was written by Robert O’Callahan who [blogged](http://weblogs.mozillazine.org/roc/archives/2005/06/eclipse_cdt.html) last summer about the promise of using the CDT for Mozilla development. At the bottom of this new article is a list of issues with using the CDT on Mozilla, a lot of which we are still working on and will feed into our CDT 4.0 requirements for next year.

I was also pleasently surprised when I went to take a look at the [install instructions](http://www.cs.wustl.edu/~schmidt/ACE_wrappers/ACE-INSTALL.html#eclipse) for ACE & TAO, a pretty big communications framework written in C++ that users have reported problems with in the past. In those instructions are instructions on how to use the CDT to develop ACE applications. Very cool.

It’s hard to see how widespread the use of the CDT is out there, at least from where I sit in here. These two examples certainly have certainly opened my eyes a little. Now back to addressing their scalability problems…


