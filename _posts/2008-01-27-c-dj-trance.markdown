---
layout: post
title: C Dj Trance
date: '2008-01-27 10:37:00'
---


Believe or not I’m a big fan of hard rock music. It started with Iron Maiden, etc. in the 80s and moved to Nirvana, etc. in the 90’s and with The Cure all throughout. It’s what I call my “angry music”. Not that I’m an angry guy, but I just love music that challenges me that way. But these days, no one knows how to play guitar anymore so I need to find my angry music elsewhere.

I have to thank my former colleague Johnny C for introducing me to Trance music. Electronic music has also always been an side interest of mine, but I’m a guitar hack first (a favorite memory recently is jamming with Eclipse’s very own Steve Northover one night). However, I’m a geek firstest, so any chance to involve my passion for music with computers, I’ll all over it. And I just love the rhythms and textures of Trance.

So I had this notion that I could make my own Trance music. There’s is actually some good low cost digital audio workstation (DAW) software solutions, including a decent one called REAPER, that I’ve been playing with to see if I want to get into it. The challenge with these solutions is finding the right software synthesizers and effects to make it all sound good. But I was floored by the number of free DAW plug-ins out there. It’s quite the huge underground ecosystem.

The main facilitator of this seems to be a free SDK put out by [Steinberg](http://www.steinberg.net/24_1.html) called Virtual Studio Technology or VST. (BTW, there’s a Microsoft equivalent called DXi, of course). It was build for their own DAW solution, but they openned up the licensing to allow anyone to take advantage of it, like REAPER. I’m not sure if that makes business sense, but it is helping me get interested in digital music so I may become a customer one day.

I checked out the SDK and even got the sample plug-in to compile using Wascana. Unfortunately, they’ve released a new version of the SDK that isn’t backwards compatible so I couldn’t try the plug-in in REAPER which doesn’t support it yet. But I was able to launch the plug-in in the test host that comes with the SDK. Everything seemed to work except for the bitmap resources since I don’t think we have the gnu resource compiler hooked up in our managed build integration. And unfortunately I ran into trouble getting it to debug at all under gdb. Yet another reason to get the Microsoft debug APIs integrated I guess.

But it does look like the CDT would be a nice IDE for applications like this. With the kind of processor power and multimedia assembly instructions you need to make these audio plug-ins work well in large setups, this is another area where I don’t see C++ going away. The experience on Windows could be improved with a nicer Microsoft compiler and debugger integration. And it’s a cool way to mix my passion for software with my passion for sound in one place.


