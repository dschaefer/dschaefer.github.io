---
layout: post
title: Design like you'll be there in 10 years
date: '2008-11-11 16:07:00'
---


I probably blogged about this a long time ago. I remember watching the news conference for the landing of the Mars Spirit rover. I had watched the landing live over the web and remember the jubilation of the team members as they received the first signal alerting to the safe landing. At the news conference one of the project managers mentioned he had been working on the project for 10 years (through one previous cancellation that is, but still pretty darn good). He was beaming to see the success. And it was well deserved.

That idea entered into my book of software design philosophy: design like you’ll be working on the project for 10 years. Think of the responsibility that would mean. In 10 years, you’ll be paying for the short cuts and short sightedness. So don’t.

Well preparing for my talk on static analysis and refactoring for Eclipse Summit Europe next week (yeah a bit of a late start, it’ll be great, though), I finally have my own version of this story to tell.

6 years ago, my good colleague and friend, John and I started down the road of building a C++ parser for the CDT. My mentor at the time thought it was a crazy idea but we had a feeling that we could do it and we plowed ahead and actually got it to work. The parser allowed us to build a more accurate way of populating the Outline View (via the CModel). It then lead the way to indexing to allow for C/C++ Search and Open Declaration to work well. It was tough and we fought the performance battles for most of it, but we soldiered on.

Somewhere along the way we started dreaming of C/C++ refactoring a la JDT. Everyone thought that was a crazy idea (despite secretly wanting it too). With all the madness of the C preprocessor mucking with the source code before it gets to the parser, how could you properly create the TextEdits that the LTK (which the JDT guys generously pushed into a common plug-in, BTW), needed to do the refactoring?

Well John put in a lot of effort and forethought and created a way to map AST nodes to location objects which allowed you to unravel where all the text came from to create the node. It wasn’t perfect, but it was a start. And unfortunately due to the untimely end of our funding, we never got to finish it.

Well, I finally got a deep look at the work that Emanuel and is team at the HSR Hochschule für Technik Rapperswil have done on the CDT refactoring engine and early refactorings. Following it through the debugger, I hit it, IASTNodeLocation – that work that John had started years ago but never got to see in action for what it was intended for. It’s been fixed up by Emanuel and CDT Indexer Master Markus, but it was doing what we had dreamed about many years ago. Weird, but it actually brought a tear to my eye.

But it really does prove the point. Design as if you’ll be working on a project for 10 years. Even if you end up not being there, someone will be, and your work will live on, and it will be much appreciated.


