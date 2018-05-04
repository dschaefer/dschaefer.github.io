---
layout: post
title: Can an LGPL Qt give C++ a lift?
date: '2009-01-22 21:07:00'
---


Black Duck recently announced their [top Rookie Open Source projects for 2008](http://www.blackducksoftware.com/news/news/2009-01-21) which using a bit of a weird metric, revealed the top 10 open source projects that were created in 2008 that had the highest number of releases. More releases makes you good? O.K…

Anyway, the most interesting information from their news release was the stats they gathered on what programming languages these new projects were using. To the surprise of many, 47% of them were written in C (C Rules!). That was followed by 28% in Java and 20% in JavaScript. It’s pretty interesting there was so much JavaScript usage. And again, these were projects that have just been created. But when you look at it, most open source projects target Linux, and by far the most popular language for Linux is still C.

One thing I noted, though, was that C++ wasn’t even mentioned. It could be that they lumped C++ in with C, but I have my doubts. I rarely do see C++ in open source. The large open source game engines, like [Ogre](http://www.ogre3d.org/) and [Irrlicht](http://irrlicht.sourceforge.net/) as well as Firefox (of course), are in C++, and OpenOffice is written in every language imaginable including C++, but I see C way, way more.

[Watch out, bad segue ahead…]

I spent part of last weekend taking a deeper look at Qt, with its upcoming spanking new LGPL license. I have to admit I’m a GPL library bigot and kept away from Qt because of that, but boy do I regret that now that I’ve seen it. It’s an incredibly complete C++ library for building apps of all kinds. And it has everything I’ve been looking at lately, WebKit, JavaScript (well ECMAScript but that’s the same thing), and OpenGL, and incredibly smooth integrations between those and many more components.

So as Qt makes this transition, I have a feeling it’s going to gain in popularity everywhere. And I think it’ll show the power of C++ and pull a lot of the developers writing for the C-based GTK away. Heck even [Ubuntu is thinking of switching](http://www.linuxdevices.com/news/NS2771709401.html) to it for their mobile platform.

Kudos to Nokia for making this decision. I think it’s going to pay dividends for them as developers take a fresh look at a great framework. Which, BTW, means there will be more developers working in the same environment that also happens to run on Nokia’s phones ;).


