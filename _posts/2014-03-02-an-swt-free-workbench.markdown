---
layout: post
title: An SWT-free Workbench?
date: '2014-03-02 00:09:35'
tags:
- eclipse
---


As a few of you know, I’ve been working hard at trying to get the Eclipse IDE to run on JavaFX. Most of the work has been done by Tom Schindl but I was massaging it to be a real SWT port, just like the ones we have for win32, cocoa, gtk and others. I don’t want there to be a lot of magic since my first goal is to get the Eclipse IDE built and running using the platform maven build. It’s got to fit a certain structure.

But the more I try and get the various Platform UI plug-ins to play nice with the port, the more I’m getting pretty tired of fighting it. SWT really is a fundamentally different beast that makes a port to a modern UI framework a very difficult task, especially when they leverage hardware accelerate renderers where you really shouldn’t be playing with the event loop like we do all over the place in the Eclipse workbench. We do need the SWT port for existing plug-ins, but the workbench?

No, I’m pretty convinced now that the correct path is to get the Eclipse workbench to be a fully e4 thing and use JavaFX renderers to, well, render it. I was surprised when I started looking at e4 for the IDE that the workbench isn’t actually fully e4. In fact, it’s a lot not e4. I’ve been told it was just too much work to get it there in the short term. And, yeah, it is a lot of work. So I can’t argue with that.

I think it’s time for me to get involved with that. JavaFX is important to me in order to give our IDE a modern look and feel and make it fully skinnable. The CSS support in JavaFX is outstanding and I love the fact you are building a scene graph for your UI and then feeding it to the GPU to render. That’s should make it very responsive and give us a chance at doing some cool effects (as long as we’re not careful not to be too cool, wiggly views anyone?).

To get there, we need a pure JavaFX workbench. Am I going to be in over my head? Well I’ve heard a lot of interest from members of the Eclipse community. Working together I think we can get there. And I firmly believe, we need to get there.


