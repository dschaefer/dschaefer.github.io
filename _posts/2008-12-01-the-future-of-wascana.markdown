---
layout: post
title: The Future of Wascana
date: '2008-12-01 10:40:00'
---


For those that don’t know, I’ve been working on the side on a complete open source IDE distribution for Windows called [Wascana Desktop Developer](http://wascana.sf.net/). It includes the CDT and the MinGW tool chain and a handful of libraries that enable cross platform development. I did the original “beta” release over a year ago and have over 12,000 downloads to date. But it’s getting long in the tooth and I really need to respin with Ganymede Eclipse/CDT and gcc 4.x.

The question I’m dealing with now is what Wascana should look like going forward. My Wind River team and I are just wrapping up a p2-based installer for our Wind River products that are similar to Wascana but on a much bigger scale and targeting our Wind River platforms. We’ve learned a lot about how to extend p2 to manage the install, update, and removal of archived binary files into an install tree.

I want to bring that similar experience to Wascana and have started working on an open source version of these extensions. I’m starting doing it as part of the CDT since I need to support CDT 5.0.x with it and want to release around Christmas time. Once I check it in, the p2 team can look and see if the want something like this and give feedback on changes that would be needed to get it into an upcoming platform release.

In the end, Wascana will mainly be a p2 repository that ensures you have all the plug-ins installed to get a working CDT for MinGW, and that will allow you to download and install the MinGW tool chain and libraries, either from their home locations, or from the Wascana SourceForge download area if I need to rebuild for whatever reason. Updates and new components would be done by adding them to the repository.

So the question becomes, do I need an old time installer for this, or would the community be happy simply downloading the [Eclipse C/C++ IDE package](http://www.eclipse.org/downloads/packages/eclipse-ide-cc-developers/ganymedesr1) and working with the Software Updates tool to get everything they need. I have a feeling people will still be looking for that single setup.exe download to set everything up. Then I need to ask whether laying down the bits is sufficient, or whether I need to do a [p2 director thing](http://wiki.eclipse.org/Equinox_p2_director_application).

The good news is that I sense MinGW is maturing. Despite having an unmanaged release cycle (and I do have a second source for the mingw gcc tool chain thank goodness), it looks like it’s ready for prime time, at least for my little distro. Enough so, I’m giving up on Windows debug support. My focus is cross platform, and my time is limited and building a pure Windows debugger is hard and without a significant contribution it won’t happen, so I’m not counting on it. Wascana will do just fine without it.


