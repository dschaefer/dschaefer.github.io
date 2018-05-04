---
layout: post
title: Eclipse CDT, More than Just for Writing Code
date: '2007-08-01 09:52:00'
---


I think I’ve gotten more Google Alerts about “Eclipse CDT” in the last couple of weeks than I ever have. It’s a great sign that people want to talk about their experiences, good or bad.

The latest one I got was from something called the [“Reality Factory 2 Development Weblog”](http://rf2-dev.spaces.live.com/blog/cns!33114F671097246!136.entry). The author had struggled with the performance of CDT’s content assist in Callisto, and I understand why. In Callisto it did a full parse including all the header files included by the file in the editor, which for C++ with lots of templates and stuff, it took quite a while. In Europa, one of the features my intern worked on over the winter was to migrate this to use the index for the contents of the header files. It’s way faster, and the author was very happy to see it.

It’s also interesting to see the comparisons with Visual Studio. The author states that in many cases, Eclipse and the CDT are actually faster than VS and he’s switched back to Eclipse. That’s cool to hear. It’s been a while since I used Visual Studio regularly but it’s looking like we’re reaching one of the bars we set for ourselves of being as good as VS (being as good as JDT is the other one, BTW). This makes me believe even more that [Wascana](http://wascana.sourceforge.net/) is important as a path for VS users who want to switch to Eclipse with all the components they’d expect of an IDE. This is definitely one of the main growth areas for the CDT I see in the coming years.

And the author of the blog entry really brought home why that’s true. It’s not just Eclipse and CDT’s support for writing code. It’s all the other plug-ins available to developers to help them in all areas of software development, including managing bugs with Mylin and source code repositories with Subversive. Even the built-in web browser gets kudos for helping out. Taking a look at the big picture of the Eclipse ecosystem, you really do get a sense of the value proposition of Eclipse. Embedded and enterprise developers get it, and we just need a vehicle to get that to the desktop developer too.


