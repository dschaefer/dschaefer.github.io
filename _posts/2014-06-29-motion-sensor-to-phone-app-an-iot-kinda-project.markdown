---
layout: post
title: Motion Sensor to Phone App - an IoT-kinda Project
date: '2014-06-29 14:41:16'
tags:
- eclipse
---


My son Alex is autistic. That presents a lot of challenges for my wife and I and, of course, for him. He’s generally at peace, but suffers from a lot of anxiety in situations that are new and he really wants everything to work out OK. We also have a very nice backyard with a gazebo on the deck and days like today, my wife and I love to sit out there. But from there we can’t see if someone comes to the front door and we don’t want Alex to have to deal with solicitors or what have you giving him a situation he can’t handle.

So that was the germ of an idea, which of course for me, has grown to a pretty big hobby project (with work implications, of course). Searching for possible solutions, I ran into the Adafruit website which has some great tutorials on how to build gadgets for this very type of problem. [They sell a motion sensor for $10](https://www.adafruit.com/products/189) that I could place on the front porch somewhere to detect when someone came up (not everyone rings the door bell and the motion sensor is more interesting).

Now, I want the motion sensor to raise a notification on my phone when someone triggers it. Very cool problem for we architects to have to solve. First do I go Arduino, Raspberry Pi, or BeableBone? Given the simplicity of the hardware, a single sensor, doing a board that has a GPU and HDMI out seems like ridiculous overkill. So I’ve gone Arduino and bought an Uno as well. I love the Arduino because it gets you into the core of the embedded world. There’s no OS, just bare metal and your code, and a few library functions to get you going. Everyone with a computer science degree should have had to do something with an Arduino. It’s the absolute core of what computers are.

Next up, I have this web site, cdtdoug.ca, which I host on DigitalOcean. It has an nginx front end to WordPress for this exact purpose, to host web apps as well. So I want my phone to connect to it, and the motion sensor so I can find out when it gets triggered. Adafruit sells a wifi shield for $40 which is supposed to be good. But to start, I’ll just use the serial port on the Arduino to send messages on my laptop and have a node.js server that forwards it to the server.

On the server, I’m going to use vert.x. I notice a few Internet of Things type projects that are using it. The plan is to have a vert.x vertical to watch for REST calls coming from node.js and eventually from the Arduino itself with the wifi shield. Phone apps will connect to the server using websockets managed by another vertical so that when the sensor triggers, it can send in a REST call which gets forwarded over the vert.x event bus to the websocket server which can the forward it to the phones. It’s beautiful in it’s simplicity and in the minimal amount of code I need to write to actually get this to work.

[![MotionSensor](/images/2014/06/MotionSensor-300x165.png)](/images/2014/06/MotionSensor.png)

So it’s projects like this that feed my passion for the Eclipse IDE. I want to be able to do all of this from a single workspace. CDT to do the Arduino code, Nodeclipse to do the node.js server, m2e and JDT to do the vert.x server, and ADT for the Android app and Thym for Cordova. If I’m missing pieces, I will build them and make them available. A proper Arduino CDT port is first on the list. I’m also curious how easy it is to do vert.x development in Eclipse. And everything needs a good debug solution from end to end (which may be a challenge on the Arduino since it doesn’t have an OS). This would be a great showcase for the Eclipse IDE and it’s place in the Internet of Things. I’m going to do my best to get this working. More in future posts.

P.S. I hesitated to call this an Internet of Things project. Designs like this have existed forever. They were just industrial automation systems with reporting to a central server. But if it gets me noticed, then while in Rome…


