---
layout: post
title: Mylin &amp; CDT destiny
date: '2008-03-18 18:34:00'
---


It’s an interesting phenomena at Eclipse how bug reports get to be famous. It’s how issues are raised, where discussions on solutions take place, and patches get attached. There are famous bugs in Eclipse that I’ve heard about and finally, I think we’ve got one on the go for the CDT. It’s [bug 162558](https://bugs.eclipse.org/bugs/show_bug.cgi?id=162558), the Mylin bridge to the CDT.

I’ve heard great things about Mylin for a long time. An old colleague of mine raved about it. I tried it and it has a great Eclipse interface to a number of different bug systems. But today, I learned from Mik’s talk about the task management features that Mylin provides and how it cleans up the UI to help you focus on what you are working on. It’s a different way of working, but I can see that once you adopt it, it’ll give developers a huge boost in productivity especially when they are working on multiple things at a time.

We’ve had bug 162558 around for a long time which asks for CDT support in Mylin’s task management system. I think there was concern that it would be a lot of work and CDT developers have always had other things to work on. But Mik promised on the report that it would only take 2-4 weeks. And now we have Jeff Johnston from Red Hat who has signed up to help and has a new plug-in ready to show.

I really think that this is a hugely important development for the CDT. In the C/C++ world, our biggest competitor is still emacs/vi and make, i.e., the command line. It’s too easy for new CDT users to get frustrated and throw it away and go back. Much more so than Java developers, for example. Ever write java code with command line tools? It’s a lot easier with C/C++ where the tools have been optimized to work well on the command line.

We really need to show the value that will pull users through the learning pains of adopting Eclipse (mind you we need to address those too) and tools such as Mylin can do that. You won’t find a command line version of Mylin. So we’ll work hard to get the CDT Mylin bridge into CDT 5.0 for Ganymede. It’ll be a fun thing to add to my CDT demos and hopefully can convince more people to use the CDT.


