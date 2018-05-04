---
layout: post
title: CDT Summit Half-way Point
date: '2007-09-26 12:18:00'
---


Well, we’re half done the CDT summit. We started with some general discussion on CDT project management and planning for Ganymede. We’ve picked 5.0 for the CDT version number. That comes with the commitment to finally manage our APIs so that the community can rely on them and read documentation about them.

We’ve had a long discussion on various aspects of debugging. The good news is that the Debug Services Framework that the Device Debugging project is working on will become much more tightly integrated with the CDT. There’s been some good work on the GDB/MI integration with DSF and we’ll have an interesting decision to make around the February timeframe whether to make this the default gdb integration mechanism for the CDT packages at Eclipse.org.

Another interesting requirement we are hearing a lot is the need to reduce the dependency that Eclipse has on Projects and Resources. Features like project-less debugging are important to users in both embedded and desktop communities. The focus is on the activity, i.e debugging, and less on working with projects and build settings. The debugger drives what files you are working with, not the user. Along with the need to support Visual Studio’s ability to add to and remove files from projects without changing the underlying operating system in an easy manner are very important.

So while we really don’t have any big new features coming, other than refactoring which we haven’t heard to much about yet and the people working on it unfortunately weren’t able to make it. We are becoming more focused on making users feel more comfortable with the CDT. And that includes users who are coming from the emacs/vi world as well as other IDEs. That’ll be a good challenge.


