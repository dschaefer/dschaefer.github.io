---
layout: post
title: CDT 3.1.2 Now Available
date: '2007-02-16 13:55:00'
---


It’s been a pretty busy week as we are getting two releases together pretty much at the same time. The first is the release of our latest maintenance release CDT 3.1.2. Bugzilla tells me there were 101 bugs fixed in this release, which is a pretty good number given that we have been very busy working on CDT 4.0 at the same time.

The biggest fix that I put in was to move away from using memory mapped files for the Index (also known in some circles as the PDOM). Memory mapped files worked well until we started running into very large workspaces where we started to run into limits on Windows. I’ve switched it to regular files that read in chunks at a time and use a least recently used (LRU) cache to make sure we don’t take up too much memory. It did cost us some in performance, but I’m still within the targets I had set out for CDT 3.1, i.e. indexing Firefox in under 20 minutes.

More information can be found on the [CDT Website](http://www.eclipse.org/cdt).

Stay tuned for our first real milestone for 4.0 early next week…


