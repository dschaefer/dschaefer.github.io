---
layout: post
title: Blogging QNX
date: '2016-05-11 10:47:06'
tags:
- eclipse
---


I’ve been working on the Eclipse CDT project for a really long time now. It started in 2001 when I fell into an opportunity to pursue my dream to work on a C/C++ IDE and, in particular, coming from the modeling world with ObjecTime Developer and Rational Rose RT, create a C++ parser that can build up a model of user’s code. I have been extremely lucky do that and to represent my various employers over the years on the project and am very proud of what we in the community have built and continue to build in the CDT.

Over the last couple of years, I started to get curious about what our users were doing with CDT. One of the ironies of working on a C/C++ IDE written in Java, you actually don’t get to use C++ very much other than the odd hello world tests. So I started to get deeper into the world of embedded systems. It started with Arduino and the world of microcontrollers. These are amazing little devices that let you build systems that interact with the real world with inexpensive hardware that brings me back to my youth and the 8-bit processors of the day. And, of course, being the CDT guy, I started working on a plug-in for CDT that helped you program these little things while showing off CDT’s latest features, the Arduino C++ IDE.

I recently bought a Raspberry Pi 3 to take things up a notch. It’s a little powerhouse that’s really not much more expensive than an Arduino and I’m thinking it would make a great platform for robotics. I can imagine putting some ultrasonic sensors on the sides and a camera on top and doing some image processing so the robot can drive some motors and find it’s way around a room of obstacles. But the thought of doing such real-time processing using Linux made me gag. I work for a real-time operating system company and I guess I’m really believing in what we do and really should be using QNX for that.

Well that has me now deep into the world of creating a Board Support Package, BSP, that will let me run QNX on the Raspberry Pi 2 and 3. It’s been a blast and I’ve learned so much about the operating system I’ve been writing an IDE for all these years. And it’s about time. It’s a very different world and have even had to learn ARM assembly language.

Being the blogger that I am, I’ve decided to spend more time writing about that experience and to share it with developers working with QNX, or interested in what we do, or simply learning about real-time software development and maybe a little IoT. I’ll still blog about the Eclipse IDE pieces I’m working on and will share those with the [Eclipse Planet](http://planet.eclipse.org/planet/). But if you want to follow along the QNX side too, I invite you to subscribe to my blog using the form [on the main page](http://cdtdoug.ca).

It’s a new chapter for me. But it fits well with everything I’ve done over the years, doing what I can to help developers make better software with great tools but now also expanding that embedded systems and their run-times. I have some really cool projects, like my robot, that will help me focus on a specific group of developers who are also working on some really cool projects and I can’t wait to get started.


