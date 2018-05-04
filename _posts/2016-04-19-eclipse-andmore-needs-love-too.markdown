---
layout: post
title: Eclipse Andmore needs love too
date: '2016-04-19 11:18:26'
tags:
- eclipse
---


I posted a tweet the other day after seeing yet another election for a new committer to the Eclipse Platform UI project.

![](http://blog.vogella.com/content/images/2016/04/tragedyofthecommons1.png)

They are doing a great job down there and they rightly took the tweet as a compliment. But my point was more that a great Eclipse IDE also depends on having great support for the platforms our users are building their software for. And the one that has me particularly concerned lately is Android.

When Google threw their support towards IntelliJ and the new Android Studio, the Eclipse contributor community went into shock. Aside from J2EE, the Google Android Development Tools was a source of pride and a showcase for the great things Eclipse can do. To be slapped in the face like that woke us up to the real problems we had of which there were many ranging from a user experience that dated from the long gone era of Windows MFC apps, to community issues as plug-ins developers had to deal with new requirements that the Eclipse SDK team never had to face. And it’s great to see teams like the Platform UI team growing and helping to address those.

For our part, a small band of us made an attempt to “rescue” the ADT plug-ins. We forked them and brought them to Eclipse as the Andmore project. It was really the heroic effort of Dave Carver who managed to get the plug-ins in shape and get them through the Eclipse IP process and get the project started that we have Andmore today.

But we’ve had a really hard time getting any momentum on it. There are a few contributors that have dropped by and it’s greatly appreciated. But Dave has moved on to a new job and hasn’t had much time to spend on it. And without active leadership, I fear Andmore will fall into dormancy and we’ll lose the opportunity to bring Android developers back into the Eclipse family where they can enjoy all the great work the Platform UI team has been doing.

I always hoped I would have the opportunity to help Andmore and it’s still on my long term plans to jump in more. But as things stand now, it’s only a side project for me. And I have much more pressing side projects I need to get done. I’ve been getting back to my roots in the embedded space and am working hard to put together an Eclipse package that can be used by electronics students and hobbyists who want to program their Arduinos and other microcontroller boards with CDT and to get them hooked on the wonderful world of Eclipse.

So I’ll leave this here. There are a few things that I see Andmore needs to be competitive with Android Studio. It doesn’t need to beat it, but it needs to be a credible alternative, especially for developers working on projects where Android is only a part of a bigger system that is being developed using Eclipse.

### Gradle Support

The Android SDK comes with first class build support with Gradle. If you want to build a modern Android project, you have to use Gradle. It’s not even up for debate. For my Eclipse IDE for IoT talk I managed to get a simple implementation of Gradle support for Android working. It was pretty easy. But it will be a challenge to get it integrated into the existing Andmore plug-ins.

### Keeping up with the SDK

What Google probably thought was a good idea, they’ve been able to reuse a number of jars from their SDK in the Eclipse plug-ins. The problem is that those jars are external dependencies and every time they up-version them, we need to bring them back through the Eclipse IP process and re-import them into the Andmore builds. It’s a serious amount of work. I just wonder if we can reduce that dependency and leverage more out-of-process communication to make the architecture easier this way.

### The Real Tragedy of the Commons

I’ve seen the term “Tragedy of the Commons” used incorrectly in relation to my tweet by a few people. [You can find the real definition on Wikipedia](https://en.wikipedia.org/wiki/Tragedy_of_the_commons). Eclipse’s version is that many plug-in developers have built their plug-ins with the assumption that theirs is the only one installed and the users only care about them. They add menus and toolbars wherever they want, and especially in highly visible places where users can find them. Better yet, they pop up dialogs to warn users of configuration issues on startup to urge the user to resolve them before using the IDE.

What would that look like if every plug-in did that and users installed them all at the same time? (And I know Eike Stepper has tried this and produced a monster!) That’s the Tragedy of the Commons for Eclipse. Plug-in developers have to think of the common good, of all the other plug-ins out there in the Eclipse ecosystem and to make sure their plug-ins play well with those.

Well, Andmore has a few issues in that regard, especially with dialogs on startup. Yes, I know my Android SDK isn’t installed, yet. I’m busy with something else. For me, it’s one of those design issues where instead of a “don’t show again” checkbox on the dialog, I want a “don’t have ever showed this dialog” one.

I truly hope that a segment of the Eclipse community will feel that supporting Android development with Eclipse is important. Hell, I think supporting iOS is important too. We can’t be the IDE for everything without having support for the big things. I’m glad we’re addressing the common UI pieces in the Eclipse Platform, but as I tweeted, the whole Eclipse IDE stack needs that love too.

 


