---
layout: post
title: I have a dream, an Eclipse UI dream.
date: '2014-08-15 16:43:29'
tags:
- eclipse
---


Humour a madman for a second :).

A few months ago, I was pretty excited about the prospect of Eclipse running against a modern UI framework such as JavaFX. Modern applications have a flow or liveliness to them. They aren’t just a bunch of toolbar buttons and menus that take umpteen clicks to do the things you want to do. They move with animations and effects that make your app feel alive. Not everyone agrees that’s what an IDE needs, but I’d like someday to take the time and experiment to see if it does.

And I’ve seen some of what’s possible. [Cole Markham’s talk at EclipseCon](https://www.eclipsecon.org/na2014/session/modernize-your-real-world-application-e4-and-javafx) this year on using the JavaFX e4 renderers for the RCP apps he was building showed the potential. His apps are beautiful and much thanks to the CSS capabilities and animations in JavaFX. It can be done and it can be good.

But what of the Eclipse IDE? Originally I thought we could port SWT to JavaFX and then introduce JavaFX slowly into the vast collection of IDE plug-ins. From Tom Schindl’s great work on this and his experience with it, I’m not sure either of us, or anyone for that matter, thinks it’ll really work. The paradigms are just too different. Maybe JavaFX can evolve to make it closer (and it is indeed still a young API), maybe not.

Where to then? I sometimes go down a dark path looking to too see where the next revolution in IDEs would come from. Eclipse was quite disruptive back in 2000 and had great success. But have we reached a stagnation point forced on by the architecture and tragedy of commons it has brought onto us (without standards and with uber flexibility, every plug-in has been free to implement their own UX and many have)? Will IDEA lead the way with it’s better funding? Will QtCreator take over the C++ world? Or is everyone just happy with their text editors and command line tools that we’ll regress back to the 1990’s?

Well, if there is to be a revolution, a new IDE framework that will fix all that’s broken with the existing ones, I’d actually like to look back at Eclipse. Often when I explain why we have Core and UI plug-ins for all our projects, I’ll bring up that maybe one day we’d like to replace the UI with something else, something not SWT. And maybe this is it. Reuse the valuable Core plug-ins we have that support build and debugging and static code analysis and source control integrations, and replace all their UI plug-ins with new ones that use a new UI framework based on JavaFX.

Am I insane or naive to think that would work. Maybe I don’t think that would work. But I can dream. And maybe someone with the resources will think it’s a good idea and make that dream come true. Or maybe not.


