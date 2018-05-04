---
layout: post
title: Exploring Game Development with CDT
date: '2010-06-28 22:10:00'
---


Well, it’s holiday time. I’m off this week and next and it’s filled up with a family union my wife and I are hosting, but I am stealing away some time now and then and my hobby time going forward with one of my dreams, building a game engine.

Of course, it’s impossible to build a game engine yourself. So instead I am putting together a number of open source pieces and integrating them. The amount of code I need to write should be pretty small but should be significant enough to help me get some real world experience using CDT. The best way to get into the mind of some one who uses your tools and understand their needs is to actually be one for a while.

The key part of the CDT angle is multi-target development. The plug-in nature of Eclipse and CDT’s support for tool chains allows it to be used to write applications for multiple platforms. In this case I’m going to do a mix of desktop and mobile featuring Windows and Linux on the desktop side and Android and eventually MeeGo on the mobile side. Android and MeeGo are particularly interesting in that I firmly believe these platforms could eventually find their way onto desktops one day. So writing a game that targets them and Windows and regular Linux desktop isn’t really that much of a stretch. (BTW, yes, I’m purposely leaving out Apple for fear of getting trapped in the “walled garden”).

For the engine components, I’m using the OGRE 3D rendering engine that is currently being ported to Android already (very cool to see). It uses freetype for fonts for displaying text and freeimage for loading images. I’ll use bullet physics for the physics engine. There doesn’t seem to be a common audio package so this may be custom per target with my own API over top. The same may be true for input, although the OGRE samples use OIS but that would need to be ported to Android.

The final piece of the puzzle will be the blender 3d editor which is going through a re-architecture right now and is extensible using python. Create your content using blender, export it with the help of python scripts and load it up into the game engine on all four platforms. Sounds like a dream that only the pros can pull off.

We’ll see how far I get. But I benefit from it in two ways – living that dream, and getting some real life experience using Eclipse for serious application development that should lead to some ideas on making it better and maybe I’ll come up with ideas for new tools. Sounds like a win-win.


