---
layout: post
title: Palm Pre and WebKit
date: '2009-01-12 09:17:00'
---


I’ve been following the [Palm Pre story](http://www.palm.com/us/products/phones/pre/index.html) a bit the last few days. While the technical details are still pretty sparse, it appears that [one of my predictions for 2009](http://cdtdoug.blogspot.com/2008/12/predictions-for-2009.html) is already starting to happen.

My understanding, and I hope it isn’t coming from sources who are also using the same technique to guess at the architecture of this thing, is that the UI for the Palm is rendered totally using [WebKit](http://www.webkit.org/). It appears that the applications for this device are written in JavaScript and use HTML and maybe WebKit’s SVG support to render the graphics. Hell, maybe it’s even [using Dojo](http://dojotoolkit.org/) to make things look really sharp.

If this is true, then it’s going to be a great test of how well this architecture works. I have my worries about how JavaScript scales and how easy it is to write traditional GUI apps, even handheld ones, using HTML as a rendering engine. But looking at the screenshots, it looks pretty awesome.

The other thing I notice is that there is a continuing trend of making it very difficult to build native apps that draw on the screen with these things. It started with JavaME in the “old days” and is continuing today with Google’s Dalvik Java VM and now Palm’s WebOS WebKit thing. They promise the power and openness of Linux and then shut the door. It’s too bad, since a lot of these handhelds have 3D graphic acceleration in their [SOCs](http://en.wikipedia.org/wiki/System-on-a-chip), and you really need to go native to build a good 3D game or what have you.

I can’t wait to see what the Pre SDK looks like, and whether developers buy into this architecture of GUIs based on web technology. And it’ll be interesting to see how good the apps can be with it. But if they’re as good as the prerelease demos, it’s something to pay attention to.


