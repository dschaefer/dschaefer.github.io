---
layout: post
title: Historic Day for Linux Desktop?
date: '2010-11-05 10:24:00'
---


I just tweeted this, but it’s worthy of a blog entry because I think this will, or at least should be, marked as an historic day for Linux. Mark Shuttleworth, Ubuntu chief, [blogged yesterday](http://www.markshuttleworth.com/archives/551) that they are starting a transition from an X Windows based environment to the Wayland display server. That is huge news and a huge push for the fledgling Wayland project which is starting to get a lot of love lately. Intel, who employs the main developer for Wayland, already seems committed to getting MeeGo on top of it, but this move for Ubuntu all but assures Wayland will become mainstream for the Linux desktop. And I can’t wait for that!

So what the heck is Wayland and why am I so excited about it? Well I’ve been working with X Windows since my university days when X11 was spanking new. It had a great architecture that allowed the display to be hosted on a different machine than where the application ran. Back in the early 90’s that was pretty important since workstations weren’t very powerful so we still had big iron Unix servers where we ran things and being able to display them on any machine in the lab was liberating. It was the best, back in the early 90’s that is.

Then entered personal computers thanks to Microsoft Windows and to some extent Apple Macintosh. As these machines grew faster and faster, it became more economical to run your applications locally. Not only that, but the graphic architecture, where display handling was part of the operating system, allowed for the desktop environments to become rich, to the point now where we have the beautiful environments of Windows 7 and Mac OS X.

Now when Linux came along, the powers that be chose X Windows as the underlying display architecture. It made sense since X Windows is open source and it does a good job. But it is shackled by the underlying architecture that made it popular in the 90’s. As Mark put it, “I understand that it’s *possible* to get amazing results with X, but it’s extremely hard, and isn’t going to get easier. Some of the core goals of X make it harder to achieve these user experiences on X than on native GL, we’re choosing to prioritize the quality of experience over those original values, like network transparency.”

And that’s where Wayland comes it. Wikipedia describes it as “a lightweight display server for the Linux desktop. Started by Kristian Høgsberg, one of Intel OSTC member, the software’s stated goal is ‘every frame is perfect, by which I mean that applications will be able to control the rendering enough that we’ll never see tearing, lag, redrawing or flicker'”. It gives the application and window managers full control over how their content is displayed and gives them free access to the graphic hardware acceleration through OpenGL and OpenGL ES, essentially the same architecture which gives Windows and Mac their great environments.

It’s going to take some time as the ecosystem grabs hold of the possibilities. It is almost certain that other Linux distributions will jump on the bandwagon, and I’m sure nVidia and AMD will do the same with their hardware drivers. But once they do, I am convinced that this will finally make Linux a real contender in the desktop space. I can’t wait :).


