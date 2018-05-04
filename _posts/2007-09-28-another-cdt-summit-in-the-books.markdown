---
layout: post
title: Another CDT Summit in the Books
date: '2007-09-28 10:16:00'
---


By the end of the three days, it really hit home why we go through the effort of organizing and traveling to the CDT Fall Contributors Summit. While it got off to a slow start, by the last two days we were busy getting deep technically and on Thursday afternoon even browsing through source code to see how to implement some of the new features. That’s something that is pretty hard to do if you don’t have 7 or 8 guys huddled around the projector screen. And with the CDT, those 7 or 8 people come from different continents.

Aside from the Debug features I mentioned in my previous post, we got into a few key areas. The team at IBM Toronto are working on new parser frameworks that should make it much easier for the CDT to handle language variants. In CDT 4.0, we released support for Unified Parallel C (UPC) that was built as an extension to a new C99 parser. They are also looking at techniques for making the indexer even faster. I think this will be great for the C environment. I still am worried about how this will scale into the C++ world and the crazy template libraries people create and use.

We also talked a bit about remote development and how we could support it with the CDT. This is the scenario where the source code, build, and debug all happen on monster remote machines while the developer accesses them from a workstation. I think we’re still pretty cautious about making sure we don’t do too much damage to the CDT architecture to make this happen. But one key feature I think we’re all mainly in agreement on is to make sure the CDT works while all file access occurs through the Eclipse File System (EFS). I am also hoping use that to add support for Visual Studio style Add File/Exclude File so that users coming from that environment, which a lot of CDT users do, can continue to manage their projects somewhat independent of the file system.

At the end, it looks like we have a pretty good plan for Ganymede, the newly numbered CDT 5.0. There aren’t a lot of big architectural changes like we’ve had in the past. That will definitely go a long way towards bringing the CDT to a new level of maturity where we have documented and trustworthy APIs and can focus more on quality, cleaning up the Bugzilla backlog and adding more automated tests.

It really felt to me that the CDT has grown up a lot in the last year, and that’s a big thanks to our contributor community and the great collection of committers that have been involved with the CDT. Our team has really stabilized and everyone knows each other now and we really do work together well. And, of course, there’s always room for more…


