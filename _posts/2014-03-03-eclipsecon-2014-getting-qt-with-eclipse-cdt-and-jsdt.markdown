---
layout: post
title: 'EclipseCon 2014: Getting Qt with Eclipse CDT and JSDT'
date: '2014-03-03 16:18:11'
tags:
- eclipse
---


Two weeks to go. Time to get really jacked for EclipseCon 2014. I’ll be giving a talk this year on the work I’ve pretty much dedicated the last two years of my life to, properly supporting Qt development with Eclipse. It’s long been stated that Eclipse, CDT in particular, doesn’t do Qt. Well, it certainly didn’t do it well, but we working hard at changing that. Qt is the foundation for out native Cascades App UI story with BlackBerry 10 and we’re pretty happy with how that’s gone. Now it’s time to contribute back to the community to make sure Eclipse does do Qt and does it well.

This talk will go through the aspects of Qt that makes it difficult for any IDE to support it. It extends C++ in interesting and powerful ways that really makes programming in C++ a safer experience. But, the IDE needs to support those extensions and we’ve done a lot of work with CDT’s parsers, indexer, and editor features to make it so.

An important aspect of the new Qt 5 is the declarative QML UI description language. It’s actually a mix of declarative and imperative using JavaScript to add behavior for events. An obvious choice would be to leverage Eclipse’s JSDT (JavaScript Development Tooling) to support that and we’ve done so. There’s some changes we need to push upstream to make JSDT support non-browser JavaScript platforms. Along with that, we’ve hooked up JSDT’s debugger to Qt’s QML remote debug protocol, giving a pretty nice debugging experience with QML. And there are a few changes we needed to do to make that happen.

If you have an interest in Qt and how the Eclipse IDE will be updated to support it as a first class citizen, come to EclipseCon 2014 in San Franciso and see me [Thursday, March 20 at 1:30 in Grand Peninsula F](https://www.eclipsecon.org/na2014/session/getting-qt-eclipse-cdt-and-jsdt). Love to see you there and get your feedback.


