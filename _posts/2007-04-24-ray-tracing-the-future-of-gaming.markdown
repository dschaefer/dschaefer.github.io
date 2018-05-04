---
layout: post
title: Ray tracing the future of Gaming
date: '2007-04-24 09:11:00'
---


I love the Inq ([the Inquirer](http://www.theinquirer.net/)). I’m not sure who their writers are but I usually seem to find out about new things there first. Last night I read [this cool article](http://www.theinquirer.net/default.aspx?article=39101) about work going to support real-time ray tracing to render 3D graphics. After a Google search, I found the real article that this guy was referring to [here on PC Perspective](http://www.pcper.com/article.php?aid=334). It’s based on research happening at Saarland University in Germany where they’ve developed an [API called OpenRT](http://www.openrt.de/), which of course is similar to OpenGL. They also have a prototype so that you can try it out.

I remember back in university almost 20 years ago now a couple of buddies of mine that were doing ray tracing for their graphics class. The images they produced were pretty cool and realistic for the time. But it took overnight to generate one frame. Mind you that was on good old Sun 3’s, but you certainly wouldn’t think of doing this in real time, even today.

The ray tracing demos you’ll find in PC Perspective article and at the OpenRT site are amazing, though. From what I’ve read, doing shadows in current technologies like OpenGL or DirectX is very difficult and game developers almost always take short cuts, which leaves the scenes a bit unreal. But with ray tracing, it appears to be much easier and the scenes appear much more believable, which is the end goal for all 3D animation.

What’s changing is the march towards many multi-core CPUs by Intel and AMD. One of the big advantages of ray tracing it the scalability of the algorithms to parallel threads. Each pixel is determined independently of the other pixels. All you need to do is partition the screen to the cores and you get almost linear scalability in performance.

Now, mind you, the demos I saw, especially the one from the OpenRT site, used a lot of cores, mainly 32 and one was even at 48. But I imagine there’s opportunities for improvement given this early stage, and even for some hardware acceleration for parts of the algorithm. But if you were wondering what you were going to do with that quad-core furnace of a chip, here’s one idea. And it’s pretty interesting to see that [Intel caught on to this idea](http://www.intel.com/technology/itj/2005/volume09issue02/art01_ray_tracing/p01_abstract.htm) a couple of years ago.


