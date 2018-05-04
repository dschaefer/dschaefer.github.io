---
layout: post
title: It's all about the Stack
date: '2008-10-13 14:12:00'
---


Someone recently pointed me to [a presentation that Tim Sweeney](http://www.cs.princeton.edu/~dpw/popl/06/Tim-POPL.ppt) (Mr. Unreal engine) from [Epic Games](http://www.epicgames.com/) gave at [POPL (Principles of Programming Languages) 2006](http://www.cs.princeton.edu/~dpw/popl/06/). The focus of the presentation was on “The Next Mainstream Programming Language” where he discussed the challenges game developers have with performance and quality and what the next generation language needs to have to help with their problems. I truly believe game developers are at the forefront of software engineering and have the heaviest requirement set for IDEs. And that’s why I’m trying to figure out how they work.

Tim’s slides talk about the technologies that went into the game “Gears of War” and it’s a very interesting mix. While the bulk of the code is C++, there is extensive use of scripting languages as well. And, of course, most modern games make extensive use of Shading languages to manipulate vertices and pixels using the almost teraflop class GPUs we have today. So they could really benefit from an IDE that did more than just C++ or more than just scripting while integrating shader development into the fold.

The other interesting point I got out of Tim’s slides was the breadth of software libraries that they were using – DirectX for 3D graphics, OpenAL for sound, Ogg Vorbis for music, wxWidgets for 2D widgets, Zlib for compression, and the list goes on. Apparently they used a mix of 20 libraries to build Gears of War. And it only makes sense as the quality of the software components out there removes any need to build the same functionality yourself.

And I think this is another area where IDEs could improve on, integration of SDKs and automatic setup of build and indexing environments. We do a bit of that in the CDT, at least on the indexing front. And it is something we’ve talked about on the Build side but we’ve never really come up with a generic mechanism that would allow you to add SDKs to a project.

Building an IDE to help game developers be more productive would be beneficial to all users of the IDE as I think all developers run into these issues. Maybe not to the same scale but I can see how everyone would benefit from multi-language and software component management support. And, of course, I can’t see a better platform to build this other than Eclipse. If we look hard, we’ll see that we have lot of this already.


