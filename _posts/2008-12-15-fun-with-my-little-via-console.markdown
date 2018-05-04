---
layout: post
title: Fun with my little VIA console
date: '2008-12-15 21:02:00'
---


At the Embedded Systems Conference in San Jose this year they handed out little VIA embedded EPIA systems to the attendees. I’m not sure everyone got one, but I was thrilled. It has a embedded VIA processor with a chipset that includes Unichrome 3D graphics, and also include a hard drive, ethernet, VGA, four USB ports, and audio in and out. It’s a cool little unit.

<div></div>I haven’t done too much with it, but thinking about this Open Console concept (set top box with 3D graphics running Linux), I thought I’d try setting it up with some of the things I had in mind. I started by putting the Debian lenny installer onto a USB stick and installing from it. That was a little tricky until I reformated my USB stick and put syslinux on it properly. I installed enough packages to get X running with the openchrome driver for 3D graphics. glxgears ran pretty smoothly which gave me some hope I could actually use this thing to run games.

So I got adventurous and installed [Nexuiz, an open source first person shooter](http://www.alientrap.org/nexuiz/). To my surprise, this and other open source 3D games are available from the Debian package repository. So a quick little ‘apt-get’ which brought down around 450MB of game, and I was off and running. We’ll off anyway. I got about 20 seconds per frame, which makes it a little hard to even notice the thing was running.

Anyway, I tried a few other simpler games and they actually worked. I had to force myself to go to bed while hooked on [billards-gl](http://www.billardgl.de/). It was fun. But I’ve slowly begun to realize that games built for the desktop aren’t really ready to be played with only a joystick as you’d likely only have in a set top box scenario. So there would be work to be done.

I also started to understand first hand the commercial opportunity behind Linux, embedded Linux especially. Sure you can install a Linux distro and get a desktop environment up without too much effort. But try to do anything off that beaten path and you’re in for a lot of work. If you can share in that work, fine. If you can pay someone to do it for you for cheaper than you could do, even better.

I also gave up on using this little VIA box for my play-totyping (hmm, new word). I need to start getting ready for my [EclipseCon tutorial](http://www.eclipsecon.org/2009/sessions?id=248) which will help me get back into the guts of [qemu](http://www.bellard.org/qemu/). Maybe I can do a little work there to bring [GLX](http://en.wikipedia.org/wiki/GLX) emulation to it, play time permitting, of course. Or maybe I’ll shell out the $500 bucks to build a real system. Though playing in qemu would be funner…


