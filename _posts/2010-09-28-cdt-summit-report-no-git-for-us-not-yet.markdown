---
layout: post
title: 'CDT Summit Report: No git for us, not yet'
date: '2010-09-28 11:36:00'
---


We had a pretty good discussion about using git for managing the CDT source. For the community members that care, git is critical to the future success of CDT. git allows the workflows we need to allow adopters to make local changes as necessary and then deliver those changes to the CDT project as candidates for inclusion upstream. That workflow is very difficult with CVS since it requires you to set up a disjoint repository. Bleach.

So we’re pretty eager. However, at the end of the session, I got the feeling that we just weren’t ready for it. At least not yet.

First of all, there’s just the need to figure out all the workflows we want to support. I was excited at the beginning of the summer about using Gerrit code review for CDT just like the egit guys are doing. Having a system to manage code changes, to make them visible to all, and to make it easy to do code reviews, is very compelling. However, it turns out that the egit use of Gerrit was a trial and the Foundation staff isn’t ready to support it yet.

So we need to go back to square one, managing patches in Bugzilla which takes away from that fork and contribute workflow that’s bringing us to git to begin with. It does bring up the need to produce some documentation so that we can decide how we want to work and to educate the contributors on that.

That brought us to the egit plug-ins. There has been some really good progress with egit thanks to the team working on it. I’m using egit for a number of projects I’m working with, both Java and C++ and am really liking the experience. However there are still a few things lacking and defects that I’ll be raising bugs on. I am seeing a lot of exceptions when doing merges, including out of memory. I want to be able to compare branches, but I guess that’s what the Synchronization view is trying to do. But then the usability of the Sync View is very confusing.

And finally, the real show stopper for me is the lack of being able to create patches between two commits, e.g. between two branches. Again, our big workflow is to allow adopters to fork and contribute the results back to the project. They will be creating local branches and committing updates to them. So being able to create a patch between their branch and our master is a must.

At the end of the day, we’re just not ready. Once we figure out how we want to work with git, and when egit fully supports those workflows, we’ll jump on the bandwagon with both feet. Until then, we have work to do.


