---
layout: post
title: Making a UX splash for Mars
date: '2015-01-11 16:26:28'
tags:
- eclipse
---


Over the last few weeks, I’ve been putting the finishing touches on our LaunchBar contribution to Eclipse. It started out of work we did for BlackBerry Momentics. Our goal was to simplify Eclipse as much as possible so new developers wouldn’t be so intimidated by it. One of my pet peeves has always been the launch experience. The poor new users who have to dive into the fire and figure out what all those settings in the Launch Configuration dialog are, let alone learn what a launch configuration is.

After looking around at how other IDEs handled launch UI, we built a sort of “best of” and put all the great ideas together into a uniquely Eclipse LaunchBar. The LaunchBar provides selectors for launch mode, thing to launch, and place to launch it. It also provides buttons to build the projects for that launch, to actually launch, and a button to stop all current launches. You always know what’s going to happen yet easy for new users to understand but with all the power of launch configurations only a click or two away.

[![Screen Shot 2014-03-14 at 10.08.11 AM](/images/2014/03/Screen-Shot-2014-03-14-at-10.08.11-AM.png)](/images/2014/03/Screen-Shot-2014-03-14-at-10.08.11-AM.png)

I’ll write more about the LaunchBar and how you can use it in your environment over the next few weeks. I’ve retargeted the release to Mars so that I can integrate it with the PTP’s org.eclipse.remote target management system, which I’ll also blog about soon. But to give a teaser, I thought I’d show what I’m using it for today.

I’ve become a fan of Arduino and similar microcontrollers (I have my Spark Photon order in too). My next project is to produce some sort of wearable that lets you put RGB NeoPixels over you’re body along with the microcontroller and a microphone so that the pixels flash and change color to the music you’re listening too. My prototype board looks like this:

[![NeoPixels](/images/2015/01/NeoPixels.jpg)](/images/2015/01/NeoPixels.jpg)

Now, I could use the Arduino IDE to build this, but given the title of this blog is CDT Doug, you know I want to use the Eclipse CDT and things like the LaunchBar and Remote framework. And here’s what it looks like so far:

[![Screen Shot 2015-01-11 at 12.54.56 PM](/images/2015/01/Screen-Shot-2015-01-11-at-12.54.56-PM.png)](/images/2015/01/Screen-Shot-2015-01-11-at-12.54.56-PM.png)

As you can see, the LaunchBar is pretty natural. Click the Play button to “Run” “ArdunoTest” on “Uno”. Run is the launch mode, ArduinoTest represents the project for which a launch configuration will be automatically generated, and Uno is my Remote Connection to the Arduino board hanging off my USB serial port.

There’s much more to come but I’m totally excited how this is working out. I use the LaunchBar every day to launch various Eclipse run-time workbench configs and Maven jobs and now C++ project launches for my microcontroller. I can’t wait until I can get it into more people’s hands and hopefully it can help get more people excited about using Eclipse again.


