---
layout: post
title: CDT 4, now 5 MB better
date: '2007-03-28 10:30:00'
---


I was just checking last night’s CDT build to make sure our source feature got generated correctly (it did, thanks [Andrew](http://aniefer.blogspot.com/2007/03/source-feature-generation-with-pdebuild.html)!). One thing I noticed was that our run time downloads are now around 17 MBs. CDT 3.1.2 was around 12 MB. That’s 5 MB more CDT! We haven’t added any new plug-ins so it’s all enhanced feature content and improved internal data structures that’s contributing to it.

Our M6 is coming along nicely and should be released late Friday or over the weekend. It’ll be a part of Europa M6 which I think is still a week or so away. The biggest thing you’ll notice is a new New Project wizard that merges standard and managed make into a single experience. Standard make projects are now “Makefile” project types, something VS users will be familiar with, and allows us to associate tool chains with standard make projects to make it easier to set them up for indexing.

For our Windows users, you’ll see a new MinGW tool chain which uses various tricks to find your MinGW installation so there is no more need to add this to your path. Also, it uses the CDT’s internal builder to call the build tools directly so there is no need to install MSYS or Cygwin to get make and the other command line tools. This will feed into the EasyEclipse MinGW distribution that I have promised to deliver.

Aside from that, the index is more complete and has more information in it to drive all our parser based features. This also feeds into better performance for content assist and open declaration since we no longer do a full parse of the file and all it’s includes. It’s not often you get ‘oo’s and ‘ah’s over a content assist, but I did at our demo at EclipseCon.

I’ll provide more details and a pointer to the New and Noteworthy on the CDT wiki once we wrap this thing up and get it out to you.


