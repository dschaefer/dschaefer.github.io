---
layout: post
title: Guess what I missed most...
date: '2007-11-08 14:40:00'
---


For some reason, I’ve gotten interested in ray tracing (like I don’t have enough in my life to do right now). So when I found out about a project [some guy is working on called Arauna](http://www.gamedev.net/community/forums/topic.asp?topic_id=471274), I had to go look.

It was pretty cool. It looked great as far as lighting and shadows and reflections go, which is one of the best things about ray tracing. And it was rendering a scene with 70K triangles in real time with frame rates on my Core Duo laptop between 7 and 25, pretty reasonable. And with the algorithm exploiting both of the cores, it looks pretty promising as well in our near future of highly parallel architectures.

The guy had the source code for download as well. Of course, being a Windows app using DirectX, it came with Visual Studio project files. Once I figured out how to work around the project setup for Intel’s C++ Compiler, I was able to load up the projects into Visual Studio Express 2008 Beta 2. Not only was I interested in looking at the ray tracing algorithms, I also wanted to check out the state of the art that Visual Studio is coming out with compared to the CDT.

VS does have a few things that we have now with CDT 4. It has a pretty fast search for declaration, definition, and references. It seems pretty accurate, although I did notice the had the same problem we did when opening the definition of a constructor. It went to the class definition instead. Also, they have a call hierarchy tree, just like CDT 4 introduced. I guess we’re reaching some kind of parody as far as features go.

But the feature I missed most, especially when trying to learn someone-else’s code, is the Outline View. We sure do take it for granted in Eclipse-land. It’s been there forever with the CDT, starting with the original drop from QNX. With VS, I kept finding myself looking over the the right hand side of the screen to see the outline every time I opened a new file. Instead I had some useless property page staring back at me.

We’re getting more and more feedback from CDT users that are coming from the Visual Studio world. There are a few things that Eclipse and the CDT are missing and we are looking at trying to address those. The biggest one is that they want the ability to add any files and directories to a project that they want. I’m looking into a way to do that with the Eclipse File System (EFS). We’ll see if I can get my ideas working. But it’s cool to see the trend developing.


