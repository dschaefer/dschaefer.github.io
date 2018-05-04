---
layout: post
title: My Journey to Mars, Eclipse Mars
date: '2015-05-18 14:05:21'
tags:
- eclipse
---


Wow, Eclipse Mars is almost finished and it’s been very busy for me and those I’ve been working with. We have a lot of exciting new features coming and I can’t wait to get them into the community’s hands and see where they take them.

I’m going to write more over the next few weeks on each of these, but I thought I’d give an overview of what you can expect for Mars. They all stem from a common theme, make Eclipse easier to use and lower the barrier to entry for new users, especially those writing C and C++ as a hobby, the new breed of hobbyist computer engineers using $10 computers to build amazing electronics projects. New users mean a growing and vibrant community.

Here are the highlights.


## Serial Port Library

CDT has a pretty interesting native library that provides interfaces to native tools that the Java run-time doesn’t. This includes a Process subclass called Spawner that can send Unix signals, a Pseudo TTY interface (PTY) that can be used to set up terminal like interfaces to processes, and access to the Windows Registry.

One thing that is really common with these new $10 computers, especially the microcontrollers like Arduino is that you need to connect to them with a serial port to see what’s going on. For whatever reason, the serial port libraries out in the open were all GPL/LGPL and the main one, rxtx, has disappeared. Serial port programming isn’t rocket science, so I wrote my own library and added it to the CDT native feature. My first use is with the Arduino CDT covered below.


## Remote Target Management

As I was building the LaunchBar (coming up next), I needed a way for the user to select which system to launch on. I made one that was pretty simple that adapted the targets such as those we were using for QNX and BlackBerry. I then started adding features, like a View to interact with the targets and then thought about a services architecture that would add command shells, remote launching, remote file access, i.e., a full blown target management system.

Well, that reminded me of Greg Watson (from PTP fame)’s talk from a few years ago about the fact we have too many target management systems, and none of them do everything we need. So he started one that does. I decided instead of writing my own, I’d add my vision to Greg’s and come up with an uber flexible, services oriented target management system. The beauty is that it’s easy to adapt to any existing TM system. And we’ll continue to build out features and make it a suitable replacement for RSE in upcoming releases.

[![Screen Shot 2015-05-18 at 1.56.06 PM](/images/Screen-Shot-2015-05-18-at-1.56.06-PM.png)](/images/Screen-Shot-2015-05-18-at-1.56.06-PM.png)


## The LaunchBar

The LaunchBar has been the focus of my team at QNX’s efforts to fix up one of the biggest usability issues we see with Eclipse, the whole mechanism to launch the applications you’re building with the IDE. There’s been some work to improve that over the years, such as the launch shortcuts, but frankly, other IDEs do a much better job at this.

We felt it was important for the user to know exactly what was going to happen when they hit the run button. And that’s accomplished by showing the current selection, i.e. What you’re going to launch, Where you’re going to launch it to, and How you’re going to launch it. How is simply the launch modes we’ve had in the past but make more accessible. The Where relates to my work with the Remote TM system. In this day with embedded targets and cloud servers, we’re often building software that’s going to run somewhere else than our desktops.

The most important aspect what helping the user define What they’re going to launch. And really, my objective here was to make it so that the user never needs to go the the launch configuration dialog for the most common cases. To help with that, we have an automated system the populates potential What’s. By default, launch configurations are a What, obviously, and that makes the launch bar usable with existing launch configurations. But the system is flexible, and What’s can be anything, for example, Arduino projects.

[![Screen Shot 2015-05-18 at 2.00.03 PM](/images/Screen-Shot-2015-05-18-at-2.00.03-PM.png)](/images/Screen-Shot-2015-05-18-at-2.00.03-PM.png)


## Arduino C++ IDE

My first foray into the hobbyist computer engineer world was with Arduino. I bought an Arduino Uno and built a little system with a sensor and a wifi shield that was a kind of Internet of Thing. But after years of using professional IDEs, the last many being Eclipse, I wasn’t very excited about the standard Arduino IDE. Also, Arduino programming is done through this language called Wiring which, come on!, it’s so close to C++, why not teach hobbyists those last two or three concepts and “Program Your Arduino in C++ Like a Pro”.

And, hey, I know this great C++ IDE they can use. So, and this is the self serving part, I set out to build an integration for the Arduino toolchain for CDT. And it turned out pretty nice and I enjoy using it for my Arduino projects. And as a bonus, I get to use the same IDE, hell, same workspace, to program the server side of my Internet of Thing project. For me, that has always been the promise of Eclipse: One IDE to rule them all!

I have the plug-ins in CDT and they’ll be coming out in Mars. It’s really only a preview at the moment and you’ll need to have the standard Arduino IDE installed for it to work. As I was wrapping up the Mars work, Arduino released their 1.6 version and with it and pretty nifty library and BSP management system with an open data format. I plan on adding support for that system to the Arduino CDT plug-ins as well and that should eliminate the need to install the Arduino IDE if you so desire.


## The Journey Continues

As I mentioned, I’ll write a lot more about these features in the upcoming weeks. It’s going to be hard to try them without a little documentation and that will come here on my blog for now until things mature. There’s a lot more ahead as I get feedback from the community and people try to use these things in different configurations. I already have great feedback from the Red Hat JBoss guys who are trying to use the LaunchBar for WTP that’s resulted in a pretty big last minute change. But this stuff is only successful if people use it and contribute back so I’m more than willing to listen.

Also my journey into the computer engineer hobbyist world continues beyond Arduino. I have a Raspberry Pi B and I have been able to build an ARMv6 hardware float toolchain for it. We’ll likely make this the first official embedded target support provided by the CDT as an example for the embedded vendors to follow. We should have done that a long time ago.

I’ve also just purchased a couple of ESP8266 chips. They’re little microcontrollers inside a wifi chip with a healthy number of GPIO pins, all for $10 or less. The Chinese company that makes them has put out a pretty good SDK and the toolchain is again standard GCC. I need a CDT integration for these too :).

I mentioned in my note about EclipseCon that I think this is probably the most exciting time to be in the Eclipse community since they early days. So many new features and great work being done by a diverse team of really smart people has breathed some much needed new life into our favourite IDE.


