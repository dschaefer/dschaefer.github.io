---
layout: post
title: Eclipse for Digital Content Creation?
date: '2005-12-07 22:12:00'
---


At my first EclipseCon a couple of years ago, Sebastien Marineau and I met someone from the Sony Playstation development tools group. They apparently were interested in the CDT as a development environment. We’re not sure what for and they didn’t follow up, at least with me anyway. But we do see some bugs raised in bugzilla coming from playstation.sony.com.

That meeting got me thinking. Obviously most of game development, at least for PCs and the consoles, is done in C and C++. Using the CDT makes tons of sense in that environment. I even got an e-mail from someone in id Software, the DOOM people, who had some issues using the CDT (indexer performance, of course, what else?), but at least they had thought using the CDT would be a good idea.

So I looked around at how game development was done and gave some of the open source game engines a try, Ogre in particular. I was able to go through the tutorials and build a very simple game application using the CDT and importing all of the graphics files that were needed. I was able to bring the application up under the debugger and check up on things. It was fun and I wish that I had more time to play with game development and get something real working.

During my investigation, I ran accross shaders, which are little assembly language programs used to program graphic chips directly. Both nVidia and Microsoft have defined specialized programming languages that allow these shaders to be built using C-like languages. Of course, that pinged the parser dude in me and made me wonder if we could leverage the multi-language nature of the CDT to support writing these shaders. Of course, my real job prevented me from spending any time prototyping this out.

Then I took it one step further. What are all the artifacts that go into games. Not only is there C and C++ code and shader code, there are 3d models and 2d textures. My thinking is that it would be a pretty cool environment if we could bring editors for graphics and project management/build together under the Eclipse umbrella. The stuff we are seeing with OpenGL support in SWT makes this even easier. The only question that comes to mind is whether Java is the right language for this, but after trying out the snippets provided by the SWT gang, performance wasn’t all that bad. So I really think building a complete game development environment using Eclipse and the CDT makes a ton of sense. All it takes is someone with enough interest and resources to start up a project to make it happen. And it would be very cool for Eclipse’s image.

Then, why stop at game development. I thought about an old aquaintance at the University of Saskatchewan who went on to work at Pixar. Obviously they do 3d modeling there as well, so I went to their web site to look at what they were all about. To my surprise, it turns out that these guys were some of the first to use shaders. They have their own programming language for defining shaders for various things, much more than graphics boards support but very similar. And they have a super powerful rendering engine that puts it all together to make movies. I don’t think it’s a stretch to take a game development environment built on Eclipse and turn it into a digital movie production environment. Makes you go hmmm, no?


