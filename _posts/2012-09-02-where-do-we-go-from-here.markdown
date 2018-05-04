---
layout: post
title: Where do we go from here?
date: '2012-09-02 12:59:00'
---


Hi! Long time no see, or at least write here in my blog. It’s been a crazy last few years since I used to write a lot. I still dump my brain from time to time on Twitter @dougschaefer (sometimes too much – beware the drunken tweets, but yes I love electronic music at the moment). But I’m not sure why I stopped writing in the large. I love to write. It’s therapeutic and helps me work through my thoughts to make sure I’m agreeing with myself. So it’s time to start again, especially now that I’m settled in my new position as architect for QNX’s Momentics/Blackberry NDK (BB10 is going to rock, BTW).

Over the last couple of years I’ve been thinking more and more about usability. The whole idea of being in the IDE business is to help software developers with productivity and to help them understand their code better so they can make it better. Yet I still often hear complaints that our tools, Eclipse based tools in particular are too hard to learn and are very quirky, especially for native development, even with all the work we’ve put into the CDT to take a Jave-centric IDE and make it work for them.

Now some of this is just, again, quirkiness of how Eclipse manages projects and resources and builds and debug and launch. And there are things we can do there to make incremental improvements. And we will continue to do those things.

But there is something bigger, and bigger in many ways. A bigger problem requiring a bigger solution but potentially a much bigger game changer. Eclipse as an IDE is looking really old. Even with Eclipse 4, it still looks like an MFC app from the 90’s. That in itself isn’t a bad thing, but we need to understand the reasons why modern apps don’t look like that any more. It’s all about usability, about making the important things obvious. It’s about making the app visually appealing, ensuring the user is comfortable and not overwhelmed by choice the first time they fire it up. These are the things I’d like to see Eclipse the IDE exhibit out of the box. But as we all know it’s huge mountain to climb to get there requires expertise we as engineers don’t naturally by rule have in our DNA. That is: understanding the humanities, how people think, especially people not always like ourselves, empathizing with them.

So how do we start? My first reaction is to throw away every plug-in with a .ui component in it’s name. Or take everything that depends on SWT and toss it. That’s pretty dramatic and I thought way too hard if not impossible. Until, that is, I saw Tom Schindl’s work with JavaFX and [how he built a mini IDE reusing the core components from JDT](http://tomsondev.bestsolution.at/2012/06/03/about-mixing-and-matching-jdt-and-javafx/). It’s something I had thought of but he actually made it work and proved that it could be possible. The powerful core platform components of Eclipse and the language plug-ins, CDT included, can be used that way. It is one thing I’ve always mentioned when someone asked why we break out core and ui into separate plug-ins. The door is opened.

So where do we go from here? My plan is to play more with JavaFX and try out some different UI layouts and paradigms. I need to understand what is possible, how would users benefit from organizing things differently. And I can do so with the confidence that once we plug in core Eclipse, we could take this IDE we love to the next level and extend it’s life to the foreseeable future. Of course one or two people can’t do this alone. Any changes of this magnitude require a significant community, but something this exciting has the natural ability to create one. We’ll see where we end up.


