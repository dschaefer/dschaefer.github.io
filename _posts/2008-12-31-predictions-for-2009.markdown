---
layout: post
title: Predictions for 2009
date: '2008-12-31 13:06:00'
---


I’m not usually one to make predictions. It’s hard for me to tell the difference between a prediction and wishful thinking. But [this article over at the Inquirer](http://www.theinquirer.net/inquirer/news/187/1050187/what-a-techie-2009-has-in-store-for-us) (still the best place to get an honest take on the industry along with /.) got me thinking about a couple of things I think are going to be important in 2009. So here we go…

**2009: The Year of the GPGPU**

This is more a continuation of a trend but the Inq article made some great points that I think will put some spotlight on general purpose programming with GPUs. The key one, is the recent standardization of a cross platform way of programming these things, [OpenCL](http://www.khronos.org/opencl/). ATI and nVidia have already signed up to provide OpenCL support for their chips and look for Intel’s Larrabee platform to come with the same. I think there is still some software and hardware architectural things that need to be done to make GPGPU more efficient and easier to program. Look for [LLVM](http://llvm.org/) (which needs an article on it’s own) to play a role, [as it already is with OpenGL](http://www.youtube.com/watch?v=syzjQJjwpyM&feature=related), and look for one of the chip vendors to put a GPU on the memory bus shared with the CPU and make these things sing.

**2009: The year of WebKit**

Ok, yes, I’m playing it safe with these predictions. [WebKit](http://www.webkit.org/) is already the base for Apple Safari, Google Chrome, and a host of Linux based browsers, so it already has a ton of momentum. The reason I think WebKit is going to the next level, is first of all the top of the class performance of it’s new JavaScript VM (and I can’t imagine why Google would continue with V8 in Chrome). But also, I am impressed with how easy it is to create your own WebKit based browser, and how easy it is to create a Linux based platform that uses WebKit as it’s front end (launch X, launch a simplified WebKit shell in fullscreen, done). I expect to see a lot more mobile internet devices built this way. At the very least, it gives a reason for embedded developers to care about AJAX.

**C++0x won’t be C++09**

I think that’s a forgone conclusion but no one really wants to admit it yet. But look for the vote to finish this year at least. [C++0x will be an exciting evolution](http://en.wikipedia.org/wiki/C%2B%2B0x) of C++ into the next generation. No it doesn’t have garbage collection, yet, but it does have smart pointers that do the job better if you use them right. C++0x makes it easier to do a lot of things, and the introduction of closures and lambda functions and expressions will breath some life into this stalwart of the software ***engineering*** community.

Well, that’s it for now. If I think of more over the next couple of days I’ll post them. There are a lot of things I hope will happen, but i’m not sure they will. But one thing is for sure, open source is here to stay and is becoming a core business model that companies still need to understand and learn to use effectively and I will continue with my work with Eclipse and Wind River to help figure that out and spread the word.

Have a safe and happy New Year! See you on the other side.


