---
layout: post
title: The Containerization of Dev Environments
date: '2017-05-24 11:38:08'
tags:
- eclipse
---


As a veteran tools architect working for a veteran embedded systems platform vendor, we’re getting pretty good at building cross development environments. You get all the speed and integration with other native tools that today’s rich host platforms can provide. Combine that that with a good installer and software maintenance tool, and it’s super simple for users to get setup and keep their installs updated with the latest fixes and patches. It’s worked for many years.

So of course, I was a bit taken back with recent talk about delivering development environments in containers and distributing them to users for use with cloud IDEs. The claim is that the installation process is simpler. But I have to ask, while yes it is simpler for the provider, is it also <span style="font-size: 1rem;">simpler for the user?</span>

I work with embedded software engineers. Their systems are complex and the last thing they want to do is fight with their tools. That doesn’t pay the bills. And that’s why we work so hard to make that management simpler. And if you don’t have the experience creating cross development environments, it is certainly appealing to only have to worry about one host platform, 64-bit Linux, as you do with Docker which, BTW, just happens to be the easiest to support especially relative to Windows.

But do I really have to teach my embedded developer customers about Docker? How to clean up images as updates are delivered? How to start and stop containers, and in the case of Windows and Mac, the VMs that run those containers? And that’s not to mention cloud environments which are a whole new level requiring server management, especially as the developer community scales. Embedded development tools require a lot of horsepower. How many users can a server actually support and how do customers support the burstiness of demand?

So, while I get it, and as vendors take this path and as users do get used to it, I do need to be prepared to support such environments. I’ll just feel a bit sad that we are giving up on providing our users the great experiences that native cross development tools provide.


