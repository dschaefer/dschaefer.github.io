---
layout: post
title: Can we help these guys be successful?
date: '2007-08-13 08:33:00'
---


I received a Google alert pointing at [from this developer](http://www.jcornwall.me.uk/2007/08/from-visual-studio-to-eclipse/) who is making the transition from Windows to Linux. Obviously, to do so, he has to drop Visual Studio as his IDE of choice and has picked Eclipse and the CDT for his Linux work. Despite some of the difficulties in setting up the CDT, he picked it as “rivaling Linux’s best IDEs”.

This transition was one of the scenarios we thought about in the early days of the CDT that would make the CDT successful for desktop development. But it is really only recently that I am starting to see this become more and more common. I think Ubuntu was desktop Linux’s tipping point. And as Linux becomes more popular there, as the momentum in the press seems to be showing, I think there will be more and more developers looking at Linux when building their applications. And the CDT, technically, is positioned well here.

But the one thing that made me disappointed with the gentleman’s post was the frustration he had setting up the CDT to work properly for him. And, you know, this frustrates me as much as it does these people. We’ve made long strides at improving the CDT, especially in this area, but it appears the message isn’t getting out, and maybe we missed something.

And to be honest, the people that are getting the CDT from Eclipse directly and trying to make it work like this aren’t getting the support they need to be truly successful with the CDT. If you get your CDT from a commercial vendor, then you have a much better chance since the vendors generally make sure the environments work properly for their customers (we do our best at QNX to do so for our customers). But the committers working on the CDT are kept very busy by their employers, as they should, and that is making it very difficult to get a focused effort to make the CDT truly work well out of the “open source” box.

And this comes back to the Platform versus IDE debate. The CDT at Eclipse.org is a Platform. It’s not an IDE. It misses several components that make it a true IDE. Support for people trying to use it as an IDE is probably the biggest one missing. I’m trying to do something about it in open source with the [Wascana project](http://wascana.sourceforge.net/), but sometimes I get the feeling that I’m fighting a losing battle. And without success on the desktop, I don’t think the CDT can truly be Uber.

Or maybe I’m just feeling down since my holidays are over and I have a ton of work piled up…


