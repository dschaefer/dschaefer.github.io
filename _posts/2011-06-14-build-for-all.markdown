---
layout: post
title: Build for All
date: '2011-06-14 20:41:00'
---


OK, when a thought spreads out more than two tweets, it’s time to write a blog entry instead. Ed Merks tweeted from the Eclipse board meeting (I presume) about the board’s concern that if Kim Moir got hit by a bus, we’d all be screwed, or something to that affect. And it’s true. Kim is a most valuable person at release time for getting the Eclipse train out the door. Without her for the Eclipse Platform, or David for the p2 site aggregation, or Markus for the EPP builds, we’d be scrambling.

So while I don’t want to take anything away from the great work they do, I do think it’s time to move to a better system where anyone can easily jump into their shoes. Not only that, but I’d like it to be easy for anyone to be able to checkout all the Eclipse projects they need and build their own product from it. I often get questions on the recommended approach to do such a thing and I don’t have an easy answer for them.

But there are two technologies that we are currently deploying that can improve the situation immensely. And I am working on bringing both to the CDT. The first is git and the second is Maven with the help of the Tycho plugins. As an example, I’d like to checkout all the source that feeds into the Eclipse C/C++ IDE package and then from the root directory, type ‘mvn clean install’ and have the zip file come out at the end.

Better yet, I’d like to clone all the source, commit any bug in any of that source on a branch, and do a build to get a test package, or a package I can send to my downstream customers. That scenario happens all the time in open source and git is making it a lot easier to manage your local branch, while making it easier to push changes upstream. And Maven/Tycho can make it easier to send builds downstream.

But it only really works if all Eclipse projects buy in. Maven can be done in parallel with whatever build system they are using so that’s not a huge problem. Getting them all to move to git is a bigger challenge. But I see the momentum starting, especially with the Eclipse Platform project discussing moving. So I’m confident we can get there. We just need to show the value the community gets from the significant work that is required to make these changes. And then we can leverage that good work ourselves and build the EPPs at eclipse.org using the same technology.


