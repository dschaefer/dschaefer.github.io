---
layout: post
title: Linus on source control systems
date: '2007-06-03 22:56:00'
---


[I ran across this video on the weekend](http://www.youtube.com/watch?v=4XpnKHJAok8). It’s Linus Torvalds giving a talk at Google headquarters about his thoughts on source control systems and why he likes the one he made the best. I thought I was overly opinionated, but wait until you see Linus. This talk was especially relevant to me as I am currently weighing the benefits and costs of moving from CVS to Subversion.

Despite his crass style, Linus does make a lot of points I have to agree with:

- CVS sucks. SVN tries to be a better CVS, but the problems are so fundamental and SVN doesn’t make enough strides to make it much better than CVS.
- Merge is the key feature of any source control system. We’ve gotten used to CVS’s weakness at merge and Eclipse’s CVS support helps a lot. I actually think the SVN Eclipse plug-ins are a step backwards since I haven’t seen a successful merge with them yet.
- Source control systems should allow everyone write access, at least on branches. I would love it if everyone who customized the CDT could do it in our main repository so we can see what they did and make it easier to incorporate their improvements. I’m not sure that is even possible in CVS and it requires central administration at least in SVN. I guess with Linus’s GIT, allowing this is it’s number one advantage.

I’m actually a big fan of Rational’s ClearCase because of it’s ability to manage branches and merges. It was a behemoth to manage, and a lot of people found it hard to work with, but I really appreciated the ability to work in a private branch and make occasional merges back to the main line. I’ll definitely want to look at GIT and see how it compares. Of course, we would need an Eclipse plug-in to work with it…

BTW, when I visited Google during EclipseCon, I saw this stage. It’s in their cafeteria and you can see people getting drinks in the background. I wonder how many other cool visitors they get like this.


