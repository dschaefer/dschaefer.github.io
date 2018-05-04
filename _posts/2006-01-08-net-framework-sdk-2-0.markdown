---
layout: post
title: ".Net Framework SDK 2.0"
date: '2006-01-08 10:00:00'
---


So I’ve started getting interesting in C# again after initially looking at it when it first came out. It looks to me like a better Java than Java, although Java is starting to catch up with Java 1.5. And with support from the Novell lead Mono project, it has the potential to become another serious cross platform solution.

Looking inside the .Net Framework SDK 2.0, I notice that it includes Microsoft’s C++ compiler. I was wondering if Microsoft was going to update their Visual C++ Toolkit, the free version of their VS2003 compiler. It appears that this is it, although I haven’t seen it advertised as such.

Today the CDT has a lot of credibility for embedded development and on Linux. It is a little weak on Windows, despite that platform accounting for 2/3’s of CDT downloads. Most of this, I assume, is by students and people kicking the tires where MinGW/cygwin is sufficient for them. Supporting a commercial quality compiler and full Windows development would definitely be a boost to the CDT’s popularity there. All you need is the .Net and Platform SDKs, and DirectX SDK if you want to make games, and you’d be good to go.

Also, by adding some focus on .Net, we can look at C# as a potential addition to the languages that the CDT supports. For those who haven’t heard, work is being done by the Fortran community through the Photran project to add Fortran support to the CDT. I have a feeling that C# be able to reuse more of the CDT than Photran does, especially the editor, since C# is more C-like. And it is more likely to be used than the Ada support I was thinking of adding.

As with everything open source, we’ll have to see if there is anyone interested enough to work on this, but it would sure benefit the CDT’s popularity.


