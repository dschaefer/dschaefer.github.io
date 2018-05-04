---
layout: post
title: x86, the ultimate applet engine?
date: '2008-12-11 16:22:00'
---


I need to watch out or people will start calling me a Google fan boy or something (well, too late). It seems everything they come up with lately grabs my attention. And I guess it makes sense, because they seem to be heading in a different direction than a lot of people, and more in a direction that appeals to me. First Android (open mobile handset), then Google Chrome (Webkit-based browser), then the V8 C++ friendly JavaScript VM, and now, [Native Client](http://code.google.com/p/nativeclient/).

If you haven’t heard of it, it appears to be a Google research project into running secured native x86 code in a browser. Yes, we have tried that before with ActiveX and it was a security disaster. But the underlying need for high performance interactive web pages is pretty intriguing. If you could write browser applets in C++, why wouldn’t you? I suppose…

I had to try it myself. The install instructions are for Firefox, but I dumped Firefox for Chrome a while ago. It’s good that Chrome has some Firefox in it, because all I had to do was copy the plugins for Firefox into my Chrome Plugins directory (it’s hidden in Local Settings, Application Data, Google, Chrome, Application, Plugins).

I was then able to go through their little demos and tests. They’re cute and the Mandlebrot demo shows some of the power. There’s also a demo of the [open source SDL version of id’s Quake](http://www.libsdl.org/projects/quake/). It’s pretty complicated to build and I couldn’t get it working on my Windows box (mainly because I’m Cygwin-free and it seems to need it). But it’s an interesting idea, taking an SDL-based application and converting it to run in a browser (Native Client uses SDL to do audio and video). Maybe, they’ll even expose OpenGL through SDL to the native code as well. That would be more interesting.

One thing though that burst my bubble with this whole experience were the results of the performance tests that they have. The C++ version of the tests were only marginally better than the JavaScript ones. I think that’s thanks to the great job they’ve done with the V8 VM. If that’s the case, I really wonder whether this stuff actually makes sense, other than porting old software rendered games to your browser, I guess. I need to stew on that one a little before buying into this idea.


