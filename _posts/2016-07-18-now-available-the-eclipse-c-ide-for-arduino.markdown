---
layout: post
title: 'Now Available: The Eclipse C++ IDE for Arduino'
date: '2016-07-18 12:34:43'
tags:
- eclipse
---


Back in October, I released the preview edition of the Arduino C++ IDE and the response has been fantastic. I had something like 50 bug reports and lots of questions on every forum imaginable. That great feedback gave me a lot of incentive to fix those bugs and get a release out based on the work we’ve done in CDT for the Eclipse Neon release. And that is now done and [available on the Eclipse Marketplace.](https://marketplace.eclipse.org/content/eclipse-c-ide-arduino)

What’s new in this release? Well, a name change for one. I wanted to highlight that this is an Eclipse CDT project effort, not necessarily an Arduino one, so I’ve renamed it to the “Eclipse C++ IDE for Arduino.” This fits in with our strategy moving forward of providing more vertical stack support for different platforms. Expect another marketplace entry for the Eclipse C++ IDE for Qt in the next release or two, for example.

But what matters to users is usability, of course. The main new feature in this release is the Arduino Download Manager available in the Help menu. It provides a dialog that guides you through download and install of Arduino Platforms and Libraries. The metadata provided by the Arduino community has been hugely beneficial in letting me build Arduino support into CDT in such a way that new boards and libraries can easily be added. And this new dialog is your gateway into that community.

![Screen Shot 2016-07-18 at 12.14.21 PM](/images/Screen-Shot-2016-07-18-at-12.14.21-PM.png)

I’ve also done a video as an introduction. It’s only 11 minutes but walks you through installation to having an Arduino sketch running on your board outputting to the Serial Console.

<iframe allowfullscreen="allowfullscreen" frameborder="0" height="315" src="https://www.youtube.com/embed/TtPvkPpAx0E" width="560"></iframe>

As always, I love to hear from users either through forums or bug reports, especially bug reports. I have things set up to quickly get fixes to users through it’s own p2 update site. Always try Help -> Check for Updates to get the latest.


