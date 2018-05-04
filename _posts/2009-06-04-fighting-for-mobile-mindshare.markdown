---
layout: post
title: Fighting for Mobile Mindshare
date: '2009-06-04 20:39:00'
---


The more I look into what’s happening in the mobile scene, the more excited I get. The smartphone platforms really are the computers of tomorrow. They all have big (enough) screens with touch, most of them have keyboards, connectivity is excellent with both wifi and high speed 3G (Rogers in Canada says it has 3.5G, even better). Heck, they’re way more powerful than the PCs we fell in love with in the 80s.

I’m looking at this from an application developer’s point of view. If you’re a mobile app developer and you have a great idea, what platform do you target? And it’s a pretty significant choice, just like it was in the 80’s. All of the platforms have not only different APIs, but different programming languages. iPhone with Objective-C, Android with it’s own version of Java, Palm Pre with JavaScript, RIM with J2ME, and Nokia with almost everything including Flash and C++. And then you have the Linux-based MIDs such as Moblin (need to mention my upcoming new bosses :)) and Maemo which are also starting to blur the line as they start acquiring 3G functionality. In theory, you’d love to get your idea on all these platforms.

But I’m really not sure how this is supposed to happen and that’s one of the biggest challenges we have in the mobile market. I can see why these vendors want to keep their own identity. These SDKs are differentiating right now, at least until we get more apps in place. And they are fighting for the same market and would rather see developers build apps for their platform and not the other guys. So, I think it’s up to the app developers to solve this, to give them bigger markets to sell into. We’ll see how it pans out.

The good news is that, thanks to Eclipse, there is already a number of these vendors who have tooling based on Eclipse. Theoretically, you should be able to build an IDE that integrates all these tools together and least have a common development environment. And the Eclipse Pulsar mobile working group is working on making it easier to set this up.

There are some common technologies. I think all the platforms have Web Browsers that support Web 2.0 applications (and that’s all Palm Pre seems to have). And since they all have full-time connectivity to the Internet, this seems like a reasonable choice. Also the newer platforms have 3D graphic support through the standard OpenGL ES API. That might be a good choice if you have a more graphics intensive application.

The one thing that crossed my mind is whether modeling has something to offer. People who know me will find that funny as I’m quite jaded from my days working on modeling tools. But Model Driven Development was intended to address this kind of problem. I think the biggest problem with MDD was poor modeling of behavior, a must in this domain, but you can’t dismiss the potential of writing your app in a platform independent language and generating the implementations for each platform you want to support. Whoever comes up with that, and it’ll be immensely expensive to build, will have a market of confused application developers to sell to.


