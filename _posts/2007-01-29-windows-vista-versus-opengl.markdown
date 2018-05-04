---
layout: post
title: Windows Vista versus OpenGL
date: '2007-01-29 11:07:00'
---


I just finished reading Tom’s Hardware’s benchmarks [comparing Vista and XP](http://www.tomshardware.com/2007/01/29/xp-vs-vista/). I remember hearing that Microsoft was dropping OpenGL support and Tom’s confirms it with their benchmark of OpenGL apps. I don’t follow the graphics community as much as I’d like but this really has to be a blow for some of them. If not that, then it’s a blow for them upgrading to Vista.

Back on my Digital Content Creation with Eclipse soap box, I guess this kind of spells doom for the OpenGL work that’s been going on with Java and, by extension, SWT. I have always thought that it would be very cool to have a 3D modeler built on Eclipse and nicely integrated with the CDT to build games and such. Most of these modelers are built using OpenGL and probably don’t work well on Vista.

So the question becomes, when will someone build DirectX support in Java in an SWT window?

It also provides a twist for the work I’m doing on Windows development. I’ve been torn between whether Windows developers should use the Windows SDK or MinGW with the CDT. I’m not sure how mature the DirectX support is with MinGW compared to their OpenGL support, so my feeling is that the Windows SDK with the DirectX SDK will be what developers will want to use. Which means I better get that Windows SDK integration done…


