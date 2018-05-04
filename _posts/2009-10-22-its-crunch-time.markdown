---
layout: post
title: It's Crunch Time
date: '2009-10-22 11:11:00'
---


I haven’t blogged in a while so while I have my head above water, here’s a few notes on what’s happening lately.

It’s crunch time for me and my Wind River Installer team as we put the final touches on our next release of our p2-based installer. Our focus now is on on-line updates and installs which is a pretty exciting capability for our customers and support teams. I haven’t blogged much about what we’re doing there but I think it’s time to start spreading the word. p2 is a great install engine. It can be used for more things than just OSGi bundles.

Unfortunately, our p2 stuff is intermingled with older install technology and what I can only describe as “legacy” UI framework. So we can’t contribute much from that yet, but I want to switch focus and replace our legacy with a more modern framework, that we can use to replace the p2 UI that exists today. You really need to understand p2 to use the current one, and that’s not something most end users do.

There are a few other things I have my fingers in. I’m still mucking with Android and my wife gave me the idea to build puzzle games. I think that’s a great mobile app, something you can do while waiting for your next flight, or what have you. I’m still following native development for Android and plan to write a plug-in that automates the project conversion step to add CDT capabilities to Android projects.

I am also taking a look at Moblin. I bought a Dell Mini 10 and installed Moblin on it. It gives me another native platform that’s actually GNU/Linux (Android is just Linux, BTW) to understand better how to use the CDT with it. That feeds into my technical focus on the CDT which will be on build. But I need to get out of the product release crunch before I get further with that.

I also am trying to find some time to look at a WebKit SWT Browser widget. There has been some work there for the embedded web project, Blinki, and I’d like to see if we can make it more generally available. Everyone who’s deployed Eclipse on Linux knows the pain of the ever changing versions of XULrunner. I’m hoping standardizing on WebKit would solve that, but we need to see how well it works first.

Anyway, back to bug fixing.


