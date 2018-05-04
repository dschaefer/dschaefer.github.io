---
layout: post
title: Design like you won't be there tomorrow
date: '2015-09-23 11:12:45'
tags:
- eclipse
---


For Eclipse Neon, we’re releasing CDT 9.0. Yes, it’s a major release, the first one in a long time. It’s our chance to clean up a few things that may or may not affect APIs but gives us that option. I think it’s healthy and we’re communicating as best we can our plans as they evolve to the cdt-dev list.

One thing that’s bugged me is the CDT build system. Not the thing that builds CDT but the framework we have that manages builds of CDT projects. I think it’s ridiculously complicated for certain types of projects. It solves everything and is uber extensible, but if you are building an integration, as I am now for Qt projects, where the builds are simpler or done by something else, CDT just gets in the way. It’s time to fix that.

Which got me thinking. The people who contributed the most complicated frameworks in CDT are now gone. Even the companies they worked for have become mainly inactive. As a long time contributor I’ve seen the generations come and go and I see the poor people who come now and have to deal with these things. I really feel for them.

I don’t know how much longer my employers and my wife will allow me to be a CDT and Eclipse contributor. It could be for quite a while longer or it could be over tomorrow. As I look at the things I’m working on, I have that in the back of my mind. I want to leave behind frameworks that are easy to understand and simple. And if there already exists simple frameworks that can do the job, ask really hard whether I need a new framework there at all.

As I peel away the layers of the onion that is CDT, I have to ask why some of those layers are there and whether the requirements that drove their creation are really valid any more. If it takes longer to use your framework than it would be to build something from scratch, what value did you add? I don’t want people who come after me to ask those questions of me. I want to be kind to them and leave something that really helps them. And hopefully, I’m doing that.


