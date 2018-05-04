---
layout: post
title: Subversive vs. Subclipse
date: '2009-02-25 14:22:00'
---


One of the most common Google searches I see in my Feedjit log is from people looking for help in the whole Subversive versus Subclipse debate. It has always dumbfounded me why we have two efforts building Eclipse team providers for Subversion. But I’ve long given up on fighting that battle.

So as I start to dive into the code for qemu, I found myself in need of making that choice again. Some would say go with Subversive since it’s an Eclipse project. I would, but they are mired in provisioning hell with a key component for making it work being on another site due to licensing/IP reasons. That didn’t turn me on much so I’m going with Subclipse.

And so far so good, but I’ve only just checked out the repository. We’ll see how it goes if I need to make any patches, and as I keep updating. But my hope is that as it has aged, all the issues I saw a couple of years ago have been addressed.

My heart is still with distributed version control and git in particular. And there is discussions on the qemu list about moving to git. And in particular, I’m very interested in how these team providers work with the CDT and how they work with the changes were doing for e4 on the IResource front. And it’s pretty clear that these plug-ins, no matter what version control system they target, need to work well to keep our users and customers engaged.


