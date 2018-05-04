---
layout: post
title: Eclipse, the IDE for IoT
date: '2015-07-19 14:00:05'
tags:
- eclipse
---


One of my hobbies recently has been playing with my Arduino Uno. I just love how accessible microcontrollers have become along with all the little sensors and LEDs and other hardware components. It’s so easy now to make your own “smart” electronics project. Lots of tutorials on the Web and a handful of on-line electronic shops to help you get started.

What we’re also starting to see is cheap wifi chips that you can add to your project. Not only that, but chips that have the microcontroller and wifi on the same silicon and SDKs to write programs that hook up your sensors and LEDs to the internet. Anyone can jump on the Internet of Things bandwagon.

But what is the Internet of Things that everyone’s talking about? My definition is more than just accessible hardware. It includes accessible web servers and web clients as well. I have a server I pay $5/month for and was dead easy to set up. It’s small but it does what I need for now. Web development is exploding with easy to use frameworks and mobile continues to provide open, or at least freely accessible tools.

And that brings me back to Eclipse. I’m using CDT for my devices, especially as I work to make the Arduino C++ plug-ins mature enough for others to use and then add support for my other devices, the ESP8266 and Raspberry Pi. I’ve written web servers in both node.js and vert.x. The Nodeclipse plugins have helped with node, and vert.x is just plain Java and I use m2e to manage my Maven pom files and builds. And client side, well, Eclipse needs a bit of work to better support the newer JavaScript languages like React.js’s JSX and Angular 2’s TypeScript. And I’m happy to see the Andmore project keeping the Android plug-ins alive. And, of course, I have the BB10 plug-ins we’ve built as part of Momentics so I can program my phone.

That’s why I love Eclipse. I can build my entire IoT stack from device to client with the same IDE in the same workspace. I can debug the entire stack at once. We should also have the capability to navigate code from the client to device as well. What line of C++ code in my device software triggered that React component to light up in my browser? With great static analysis that a Integrated development environment can bring you, we should be able to see that.

Eclipse is uniquely positioned to be the IDE for IoT. It’s not only the technology that brings all these environments together, it’s the community. What other community has the diversity of device developers, web developers and mobile developers all working together on a common tools platform? That’s what makes Eclipse an exciting community to be a part of.


