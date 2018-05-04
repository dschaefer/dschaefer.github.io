---
layout: post
title: Looking Forward to 2017
date: '2016-12-31 18:10:38'
tags:
- eclipse
---


I know a lot of people didn’t like how 2016 turned out, especially Americans, but for me it was a year of reflection and renewal.

As the state of the art for user interface frameworks gel around hardware accelerated graphics, I have been worrying for the future of Eclipse. It’s age is really starting to show and it’s getting harder to find tools developers that want to work with it. And with the murky future of JavaFX and Java as a desktop application technology, It’s time to start looking for the next thing in desktop IDE frameworks.

I also spent a lot of the year learning more about what embedded software engineers do. I’ve been building tools for them for many years but haven’t had a chance to use them myself. As Arduino and Raspberry Pi become cheap yet powerful and accessible devices, I bought a few of them and am starting to see how fun it is to program these devices to interact with the real world.

There are a few areas where I will be focusing my time in 2017. Here are some quick highlights. One New Years resolution I definitely have is to write more so I’ll be adding details as the year progresses.


## Eclipse Two

Those who follow me on Twitter will notice me working on a new project that has grown from my fascination with [Electron](http://electron.atom.io/). Electron is the combination of Chromium and node.js in a desktop application framework. It’s what Visual Studio Code is written with along with many new and upcoming desktop applications, like Slack. It’s given me a fun opportunity to really learn HTML, CSS, and JavaScript and think of how I’d build an IDE with it. I have a couple of things running and [you can follow along here on my github account.](https://github.com/dschaefer/eclipse-two)

![](/images/Screen-Shot-2016-12-26-at-7.01.26-PM.png)

Of course people have asked why not just extend one of the many text editor frameworks, like VIsual Studio Code, for what I need. There is a big difference between text editors and IDEs. Text editors seem to focus maniacally on being just text editors. IDEs add different types of visualizations and graphical editors that abstract away some of the more complex aspects of systems development. Web developers may not appreciate it much (yet), but embedded software developers really need the help that these abstractions provide.

My hope is that this work with an Electron-based IDE bears fruit and attracts IDE developers who are excited about the same idea. I’ve called it Eclipse Two (and it’s not e2, BTW, it’s Two), since it’s my full intention that if the Eclipse community is interested, we’ll bring it there. As it was in the days Eclipse One was introduced in 2001 and CDT in 2002, we can’t build this by ourselves. It only succeeds with a strong community and with strong architectural leadership that Eclipse is famous for.


## CDT and the Language Services Protocol

The Language Services Protocol (LSP) is quickly becoming the accepted architecture that enables IDE’s to acquire language knowledge users expect as well as allows us to experiment with new IDE front ends, like Eclipse Two. Since it’ll be a few years before a new desktop IDE enters prime time, we’ll need to keep Eclipse and the CDT alive and thriving.

One thing we’re starting to see, thanks to Dr. Peter Sommerlad and friends on the C++ Language committee, is the C++ language continuing to evolve and modernize with new language constructs introduced every three years. It’s going to be very difficult for the small CDT team to keep up.

We need to look for alternative language providers and work with other IDEs, possibly leveraging the LLVM project’s libclang or some other parser that we could hook up to the LSP. That will likely be a lot of work since we rely on the CDT’s parsers for many features that the LSP doesn’t currently support but I think it’s a long term direction we need to investigate and a number of us CDT committers feel the same way.


## Arduino and the Electronic Hobbyist

I am still fully committed to the Arduino plug-ins I’ve built for CDT and will continue to enhance them as the Arduino community and the mainstream Arduino IDE evolves. I am still hoping that members of the community will help with code along with their fantastic bug reports. The feedback has been nice to see and I’m glad the plug-ins have been useful.

The more I look at the work that embedded software engineers do and the incredible complexity of the systems they are working with, the more I am reassured that these developers do indeed need the help a good IDE can give them. Of course, it has to be a **good** IDE and I continue to work to understand what that means and help make it happen.

BTW, I had started on some plug-ins I was using to program the ESP8266 I used in my demos in 2016. Since then I’ve been in conversation with the ESP32 community and it’s been great to see that they are already adopting Eclipse and the CDT. [Instructions are here if you’re interested.](http://esp-idf.readthedocs.io/en/latest/eclipse-setup.html) The good news for me is that it’ll give me a chance to stop working on my own plug-ins and to give me more time to focus on the other things in this list :).


## Use an RTOS for your Real Time system

Programming the ESP8266 gave me some experience with FreeRTOS. In the demo, I have an ultrasonic sensor that I use to trigger different colors in the NeoPixels I also have attached to the chip. All of this is very real time sensitive. I need to measure the time between two interrupts to calculate distance from the sensor, and the NeoPixel communications depend on sending a serial stream of data at a very sensitive clock rate. Real time matters.

As part of the demo, I was showing CMake and the Launch Bar and how easy it was to switch from building and launching for one system to another. I took the real-time code for the ESP8266 and pretty much ran it as is on my BeagleBone running the QNX Neutrino RTOS, including the interrupt handlers and the NeoPixel code. I can’t imagine doing that on Linux. I know I work for the company, but it really helped me appreciate the Neutrino microkernel architecture and how easy it is to build an embedded system with the tools and APIs we provide.

The problem is, not enough people know about Neutrino and what a good RTOS can offer. Too many people are using Linux in real-time systems because it’s easier to get started, because it’s what they know, not because it’s the right architecture. One thing I hope to do is to help with the cause and spread the word and make it easier for the community to try it out. What that means, we’ll have to see in the upcoming months.


## Beyond the IDE

I’ve made my career as a tools developer to do what I can to help other software developers build systems. But tools alone isn’t enough. Tools need to be combined with education through demos and tutorials and other types of instruction. Now imagine combining the two, a tutorial you access on the web that drives your desktop IDE as you learn.

And with that we come full circle as that’s one of the use cases I hope we can achieve with Eclipse Two! An IDE that not only helps you write and test code and build systems, but teaches you how best to do that as well.


## Happy New Year and all the best in 2017!

It’s going to be a great year for the Eclipse community and technology and I look forward to helping where I can.


