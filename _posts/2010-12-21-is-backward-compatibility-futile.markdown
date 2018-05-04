---
layout: post
title: Is Backward Compatibility Futile?
date: '2010-12-21 22:42:00'
---


In the last few weeks I’ve run into two products that I’m working with that try to maintain backwards compatibility with previous Eclipse releases. That is, while working on an upcoming release they want to make sure their plug-ins work all they way back to Eclipse 3.4 (one case only to 3.5, but still).

And I understand the desire of that. I’ve found old plug-ins that I want to use which claim support for 3.5 say and I’m very happy when they install and run with 3.6. And I’m even happier when the install into and work with M4 of Indigo. It’s a difficult decision to pull back from the latest and greatest to get some needed functionality. It doesn’t seem right.

But for these products, one thing should get in the way of that, the CDT. We don’t claim 100% API compatibility from year to year. There’s a reason why we’re working on CDT 8.0 while the platform is still 3.7. And there’s lots of practical reasons behind that, the main one being that we don’t want to be tied to bad decisions made in the previous release. The more external tools we try to integrate and new features and just general clean up, we need to make things better even if we have to change APIs to do it.

No it’s not fair to the community, but then we really haven’t had a lot of push back from the community to stop that behavior. We can only assume they’re reasonably happy to follow along, releasing their plug-ins with a fixed line up of Platform and CDT. And maybe that’s it. The CDT ecosystem isn’t set up where vendors plug-in their CDT integrations into each other. We tend to be competitors at that level, not partners.

But I think that is going to change very soon. Of the two products I mentioned, one is more mature and I guess CDT just happens to be backwards compatible enough that things just work. I’m a bit surprised but it relies mainly on debug APIs which we’ve been pretty careful to preserve. But without guarantees, I fear what they are doing.

The other is new and I’m kinda getting in on the ground floor. I have to decide which version of CDT to support. The rest of the stack supports back to Eclipse 3.5 which would be CDT 6. But then I want to do something good with CDT scanner discovery to properly set up the indexer. There should be some nice fixes in the upcoming CDT 8 for that. So do I have two versions of this thing? That’s kind of where it goes, which is why I’m hoping we get these APIs locked down soon, for the good of all integrators who are facing the same decisions.


