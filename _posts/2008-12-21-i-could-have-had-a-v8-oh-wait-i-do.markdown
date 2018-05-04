---
layout: post
title: I could have had a V8, oh wait, I do
date: '2008-12-21 22:30:00'
---


I’ve always been intrigued by programming languages and what makes them tick, and what is the best one for what situation. That’s why Dave Thomas’s keynote at ESE still has me thinking about the mix of JavaScript and C++. So much so that I spent a few hours this weekend while waiting out the snow storm to get [Google’s V8 JavaScript VM](http://code.google.com/p/v8/) building under [MinGW for Wascana](http://wascana.sourceforge.net/). I think it would be an intriguing addition to have the VM DLL available for developers using Wascana. With a few changes, I have it building and passing the unit tests and I have a patch into the V8 project. I’ll make V8 available in the Wascana 1.0 alpha in the next couple of days.

Now that I have it, I have to ask myself – what the heck do you do with it? I’ve thought about building wrappers for the wxWidgets library to let you build thick client apps in JavaScript. wxWidgets also comes with Wascana, and thick client apps is kinda what Wascana is all about (aside from dreams of using it for game development, which could also benefit from a fast JavaScript engine).

But it’s not clear where one would draw the line between JavaScript and C++. Given a C++ library like wxWidgets, or SDL, or what have you, is it enough to wrap it with JavaScript and have the developer do everything in JavaScript. Or should JavaScript just be this thing on the side that allows for extensibility of some larger application written in C++.

It makes me wonder if I’m following some crazy idea that some madman sold me in a bar in Germany. Or maybe this is challenging me to give it deeper thought, to think about how scripting and native languages are supposed to mix. Where in all this is the sweet spot of architectural balance. Or is there one? Either way, it’ll be on my mind over the Christmas holiday season.


