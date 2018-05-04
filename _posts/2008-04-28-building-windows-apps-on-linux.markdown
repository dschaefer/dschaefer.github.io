---
layout: post
title: Building Windows apps on Linux?
date: '2008-04-28 14:00:00'
---


I had this [interesting feature request](https://sourceforge.net/forum/message.php?msg_id=4933518) on the Wascana forum. This user would like to use Wascana on Linux to build applications that run on both Linux and Windows. You know, that’s an idea that could fly.

I noticed that a number of the [MinGW developers](http://www.mingw.org/) develop the MinGW tools on Linux. I think they are targeting Wine, the Windows emulation layer for Linux (and if any of them are reading, feel free to fill in the details). And I’ve seen a number of howto pages describing how to build the MinGW toolchain on Linux. It shouldn’t be too much of a leap to build libraries such as [wxWidgets](http://www.wxwidgets.org/) in a cross development mode, although if you make too many assumptions that target == host, that won’t work.

It’s one of the big advantages to the GNU compiler suite, it’s ability to build in a cross-compile mode. It’s what makes it so popular in embedded. And it’s one of the benefits of CDT, to be able to target multiple architectures from the same machine. You wouldn’t have to change the CDT at all other than to avoid trying to find MinGW in the Windows registry. Now if only someone would come help make it happen…


