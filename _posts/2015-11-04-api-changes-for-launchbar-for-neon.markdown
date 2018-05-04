---
layout: post
title: API Changes for LaunchBar for Neon
date: '2015-11-04 13:54:39'
tags:
- eclipse
---


The LaunchBar project that a number of us are working on is in a weird home at Eclipse for the moment, i.e. as a component of the CDT project. That makes it hard to reach everyone who’s extending it for their projects and products. Of course that’s assuming there are any, but if there are, I hope they’re following Planet Eclipse or my blog.

I have a big API change that I will be pushing tonight on the master branch. It reintroduces a concept I had a while ago but gave up when I foolishly drove IRemoteConnection as the way to model launch targets. Launch targets are the place where you want to launch. It will now have an ILaunchTarget which is a very general object, simply a name and a type identifier. And there are a few things around that to be able to match ILaunchTargets to your target management system of choice. In theory, I should be able to now push the whole launch bar to platform debug without adding weird dependencies.

The change is on the master branch which will be used for Neon. Maintenance for Mars will continue on the ‘mars’ branch. As always, let me know if you have any feedback, see any bugs, or have thoughts of where you think you could help.

Of course I need to document all of this and as I get satisfied we finally have the right APIs in place I’ll do that and help anyone who wants to use the launch bar with their launch configuration types, launch modes, and launch target types. More soon.


