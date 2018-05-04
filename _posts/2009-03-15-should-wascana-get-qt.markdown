---
layout: post
title: Should Wascana get Qt?
date: '2009-03-15 14:30:00'
---


I’ve been working on my EclipseCon talk and tutorial, which I’m really looking forward to now. Especially the talk where I hope to share some of the things I learned being involved with the CDT project for almost seven years now. And I’m hopeful it’s useful to others working in open source, especially the things that didn’t work as well as I hoped…

Anyway, while doing that, I’ve started playing with Qt, which was recently released with LGPL as one of the choices for licensing. That eliminates one of the hurdles I have for including it into Wascana, my CDT for Windows distribution. So now the question is, should I include it? Should I also keep wxWidgets? Since the Wascana plan is to become a p2-based distribution, there should be no harm in having both. It’s just that I don’t use wxWidgets so I’m not sure whether what I’m producing works or not.

Why that matters is because I build the libraries for Wascana myself using the gcc/g++ I distribute with it. I’ve switched over to tdragon.net as my supplier for gcc, mainly because they (or he?) provides the latest releases from gcc (and the mingw.org community is a bit of a mess). And I want to make sure these libraries are built with the latest and greatest optimization algorithms gcc is providing.

At any rate, I’m learning how to build Qt and it’s running right now. I hope it doesn’t melt my laptop. They have a ton of example and demo projects that I can use to test so it’s a pretty good environment for producing quality distros.

I should also look at their Eclipse plug-ins. They provide an installer for the Windows version which installs into an existing Eclipse. I wish they had a p2 repo that I could use instead. But I’ll have to see what they’re laying down and understand their licensing to see whether I can make these available in Wascana as well. I still find it weird they have their own IDE, Qt Creator, when it should be pretty easy to put together an Eclipse-based IDE that does almost the same, if not more…


