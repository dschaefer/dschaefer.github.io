---
layout: post
title: Introducing ... Wascana Desktop Developer
date: '2007-07-24 20:18:00'
---


As I [reported earlier](http://cdtdoug.blogspot.com/2007/07/whats-in-name.html), I have to change the name of “CDT for Windows” to something else. While doing so, I want to try address a big sector that I think we’ve kept trying but kept missing, and that’s the C/C++ desktop application developer.

So here it is, the [Wascana Desktop Developer](http://wascana.sourceforge.net/), or simply Wascana. What’s a Wascana? Well, since I was in Regina and I had some people comment on my last blog entry to name it after Regina, I did. Wascana is the Cree word for “Pile O’ Bones”, and was the original name for Regina. The beautiful park and lake in the center of Regina is called Wascana Park. They just finished a [cool redevelopment project](http://www.wascanalake.com/) of the lake, which was an impressive engineering achievement on a tight budget. And this distribution really is a pile of bones, a collection of open source components that we’re bringing together to make a skeleton that desktop application developers can dress up. Or something like that :).

I originally planned on addressing the needs of the Windows developer, but, given the strenghts of CDT at cross platform development, I’d like to expand this to cover all desktop operating systems, including Linux and Mac OS X. And I’d like to provide a set of open source cross-platform libraries that support a variety of desktop applications. The [wxWidgets](http://www.wxwidgets.org/) library is a natural. I’d also like to support the hobbyist game developer, one of probably the most interesting area of desktop development. Something like [Ogre](http://www.ogre3d.org/) and [SDL](http://www.libsdl.org/) would fit that bill.

I am also making my Microsoft C++ compiler and Windows debugger support a part of this project to try and get more interest (i.e. help) with it. I’ve been disappointed in the progress of MinGW, e.g., there’s still no gcc 4 port. And gdb is still gdb and has a lot of issues on Windows. So I think MSVC support needs to be there to for Wascana to make any serious inroads on Windows.

Linux will be interesting. Ideally, we’d like to leverage the tools and libraries as they come with the distributions. We’ll need to make sure we get the right versions lined up, maybe with some super packages or something. We’ll have to see.

And as for Mac, well I’ll need help with that but I know there are a lot of Mac developers using the CDT.

BTW, I’ve renamed the CDT for Windows project at SourceForge and unfortunately, the didn’t forward the old name to the new name so I apologize for the confusion and hope you can find us at [http://wascana.sourceforge.net](http://wascana.sourceforge.net/).


