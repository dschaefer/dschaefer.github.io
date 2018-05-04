---
layout: post
title: What a great first week for the Arduino C++ IDE
date: '2015-10-24 19:04:49'
tags:
- eclipse
---


As I mentioned in the introductory note, I’ve been working on the Arduino C++ IDE for Eclipse for over a year. It started out as a very simple CDT extension to deal with the Arduino toolchain and SDK. But then the official Arduino IDE came out with a new release and a new metadata system that lets you download SDKs and toolchains for the vast array of Arduino boards and libraries. I knew it would be critical for the Arduino C++ IDE to have the same feature so I spent a lot of my personal time in the summer to get it working. And I love how it’s turned out.

But I only have two boards, an Arduino Uno and an ESP8266. Luckily the ESP8266 community has added an Arduino compatibility SDK and the ESP8266 toolchain to the metadata files so that’s let me use two really different boards to test things out. But I knew I couldn’t do it without some help so I released a Preview edition with hope it would grow a community of people with different boards and projects using different libraries and give it so much more test coverage.

And have they ever! Even before I posted the howto video I had a couple of people tweet at me thanking me for it. So I rushed out the video and since then, the feedback has been awesome. 18 bugs later, 15 have been fixed and 5 updates to the p2 repo and it’s in really good shape now. Even the Eclipse Foundation’s Mr IoT Benjamin Cabé has been helping with bugs and patches and some really good feature requests.

It’s a great start, better than I could have hoped for. And there’s more to come. So please give a try if you have an Arduino family board and a cool project to build and let me know how it turns out. The bugs and interactions with the reports have been incredibly valuable and I’ve learned a lot. And thank you in advance from me and this great community!


