---
layout: post
title: Time for Distributed Source Control is Now
date: '2008-12-13 10:33:00'
---


Imagine this scenario. You’re part of a small team that’s been following the CDT closely and have adopted it as the IDE for your commercial platform. You grab the CDT source at times convenient to your product deliver schedule and work on a local copy fixing bugs you find as you go through product testing. You’re not a committer but you do submit patches from time to time and hope that the CDT team picks them up. But they’re often busy with their own delivery schedules and the patches often grow stale and fall off everyone’s radar.

So you live with your CDT fork and struggle every time you have to update to a new CDT version, so you don’t do that very often. And since you’re busy struggling in that environment, you really don’t end up with time to get more involved with the CDT. You are a small team and you only have so much time in the day. You run into Doug once in a while at the Eclipse conferences and talk about what you do and promise you’ll figure out some way to get more involved, but he knows your story too well and doesn’t put much faith in it despite his appreciate for your intentions.

Sounds like I have experience with this, don’t I. This scenario is too real and I’d bet is very common across all open source projects. Relying on CVS and Subversion at Eclipse with access controls limited to the select few committers makes it very difficult for those on the fringes to get more involved. It truly is a have/have not environment. The committers have it easy, checking in their changes whenever they want and those that aren’t are struggling to keep up, or simply fork and go their own direction.

I’ve learned that the new Symbian Foundation as selected [Mercurial](http://www.selenic.com/mercurial/wiki/) as their source control system. Along with Linus’s git, it’s one of the new breed of distributed source control systems. These systems allow for multiple repositories and provide mechanism to pull and push changes between them. The introduction chapter of the [Mercurial on-line book](http://hgbook.red-bean.com/) provides a great description of why this architecture works well for large globally distributed projects.

I invite everyone to read it, especially the Eclipse community. Because I think we need this kind of capability now. CDT needs an infusion of new blood and I know there are a lot of people who work with the CDT code base but have only a limited time to contribute back. If we had the infrastructure to better support them and make it easier to pull their changes into the CDT main line, and easier for them to keep up with everyone else’s changes, it could be the formula we need to grow.


