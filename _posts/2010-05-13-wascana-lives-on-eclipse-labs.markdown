---
layout: post
title: Wascana Lives! on Eclipse Labs
date: '2010-05-13 13:20:00'
---


When I first heard of Eclipse Labs, I was thrilled about the idea. Having a central hosting site where we can gather all the open source projects that skirt the official Eclipse site is a great way to build visibility for these projects and a great way to promote the creation of new ones.

Well, today, Eclipse Labs is a reality. And, as I was one of the beta testers for it, I’m pleased to announce that I have moved the Wascana Eclipse C/C++ IDE for Windows Developers over to it. I really struggled with Wascana over at SourceForge where there’s a low signal to noise ratio, but thanks to Eclipse Labs, it should help people find it and realize it’s place in the Eclipse community.

Right now, I’d consider Wascana still beta quality, mind you all of the packages are released open source projects so I know they work. But the key behind Wascana is a p2 repository and the org.eclipse.cdt.p2 plug-in that knows how to unpack tar.bz2 files. This plug-in is part of the Helios Eclipse C/C++ IDE package so all you need to do is get that and put the URL to the repo into p2 and install away. Feel free to hop on over and take a look at [the Wascana site at Eclipse Labs](http://code.google.com/a/eclipselabs.org/p/wascana).

In the future, I hope to figure out an even easier way to install, possibly similar to how Subversive gets it’s SVN connectors. At the very least, I’ll be posting an NSIS installer containing everything you need up to the Wascana site. This should all be in place for the Wascana 1.0 release around Helios release time.

*Update:* As I was writing this blog, an issue I was having with the downloads have been fixed. Wascana 1.0 Beta1 is now available on the site.

Thanks to Ian Skerrett and Google for getting Eclipse Labs together. As I mentioned in the blog post I posted when I first heard of it, this is going to be a game changer. I can’t wait to see what projects pop up there.


