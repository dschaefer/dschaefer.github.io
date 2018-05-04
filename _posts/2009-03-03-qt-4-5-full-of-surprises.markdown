---
layout: post
title: Qt 4.5 Full of Surprises
date: '2009-03-03 09:23:00'
---


[Qt 4.5 was released today](http://www.qtsoftware.com/about/news/nokia-releases-new-qt-developer-offerings-to-increase-productivity-and-performance). As expected, it comes with the adoption of the LGPL license which should make Qt free for commercial development if you so choose. I think this will be a huge boost to the adaptability of Qt and hopefully make an impact in the Gnome versus KDE Linux desktop wars (mind you the KDE gang are really shot themselves in the foot when they released 4.x as a planned regression from 3.x).

There were a couple of big surprises that came with the release announcement. First was the discontinuation of Qt’s embedded product, formerly and lovingly known as Qtopia, the best product name in the business ;). The plan I understand is to fold that functionality into the Qt mainline releases with the intention of making Qt a truely cross platform API for both desktop and mobile. And they’ve started by introducing an OpenGL ES paint engine into this release, which if I understand correctly will allow you to use Qt to create apps for mobile devices now.

The other big surprise, isn’t really a surprise since I’ve known about and wondered what was going to happen, but they’ve released a 1.0 version of their IDE, Qt Creator. It appears they are going forward with this IDE as a key offering, and have released it as LGPL as well. Which means, theoretically, a community could form behind it and it could start to compete with Eclipse. We’ll need to do a thorough analysis and understand what it all means. Especially since they also uprev’ed their Eclipse integration and have a beta of their Visual Studio integration available. How does Qt Creator fit into this world?

The only thing that really bugged me in their news release on Qt Creator is their claim that “it provides the first IDE designed specifically for cross-platform development”. Uh, guys. The CDT is 7 years old and counting…


