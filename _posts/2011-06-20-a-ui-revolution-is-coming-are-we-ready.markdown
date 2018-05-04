---
layout: post
title: A UI Revolution is Coming. Are we Ready?
date: '2011-06-20 20:20:00'
---


This topic has been brewing in my mind, and in this blog, an in my tweets for months now. And one final event made me certain it is going to happen. And that event was the introduction of Windows 8. Not that Windows 8 is really that big a deal. But it confirms for me a trend that’s going to change the way we interact with the desktop applications we use daily, including Eclipse. Yes, a UI Revolution is coming. And we need to make sure we’re ready, or Eclipse is going to look old very quickly.

What am I talking about? Well, let’s start at the beginning. There is no question that Apple started the revolution with the iPhone and iPod Touch. Yes, there’s an app for that. There’s an app for everything. Apps are small, easy to create with a simple UI that was intuitive even for “regular” people (and, no, computer people aren’t very regular). The rest of the world outside the walled garden got their fix thanks to Android and Windows Phone and a few others. Smartphones have revolutionized how we think of applications.

Of course, once we have smartphones figured out you want to see if the same ideas scale upwards. The next big hole to fill was tablets. Tablets have been around for a long time albeit with the old UI borrowed from the desktop. It didn’t work. But could the smartphone UI scale up to tablet sizes. Indeed. iPad is gigantically successful and Android and Playbook are following behind. We’ve finally figured out how to make tablets commercially successful by using UI that again was intuitive for everyone.

Now, as I’ve been wondering here and there, what about the desktop? Does it make sense to bring these same principles to machines with larger and multiple screens with keyboards and mice and fast CPUs and GPUs? Well, I think we hit a tipping point. And that point happened when someone got the bright idea to slap a keyboard and trackpad onto a tablet, i.e., the Asus Eee Pad Transformer. Watching the videos people have posted onto YouTube of the Transformer in action, I am convinced that a tablet UI would work just fine on a desktop platform.

And apparently, so is Microsoft, which brings us back to Windows 8. Early videos of it show off exactly that. It’s the Windows Phone 7 UI, scaled up for both tablets and the desktop. And I think it looks pretty sharp. And I don’t see any reason why Android couldn’t do the same. And with the work Nokia/Trolltech are doing with Qt version 5, I can see how we can do the same for Linux. We all love the usability of our mobile devices, I want to love my desktop just as much.

But there’s problem. Watch the Windows 8 demo when they bring up Excel. It’s revolting, but in the wrong direction. You finally see how bad the old time UI that we’ve had for decades and that has been replicated on every desktop OS we know really is. We really need to invest in upgrading the UI and potentially reinventing those applications if we want to keep them around.

And, yeah, that includes Eclipse. Unfortunately, the old technique of putting a common API over the native UI frameworks isn’t going to work. The new frameworks are just too different. And making them common looses the gains they bring individually. We got away with it before because they used to be so similar. Not any more.

So what are we going to do? There’s many ways, I suppose. The itemis guys gave a great presentation at EclipseCon on one of the strategies they used. They use a DSL that implements the logic and general layout and generate code for each of the UI frameworks they support. It was cool but I’m not sure how complex of an app you can build that way.

But I do think they are on to something. You need to program the UI in the language and technique that the framework supports. But the core logic of the application should be able to stay the same. You know, Model-View-Controller, and you only need to swap out the View part? And we should be set up for that, no? Isn’t that why we broke things up into ui and core plug-ins? Or do we have so much logic in the ui plug-ins that this won’t work?

So this is an area I’m going to try and prototype. And I’ll start with Qt5 with their QML Javascript-ish UI language and see whether I can hook up Eclipse services through some sort of QObject C++ to Java bridge and make them dance. I have a feeling it’s going to be a dismal failure. But you have to start somewhere. Doing nothing doesn’t leave me feeling very comfortable about Eclipse’s future after the revolution.


