---
layout: post
title: It's Android Time
date: '2009-05-16 19:56:00'
---


Well, I’ve had a lot of fun trying different things with embedded Linux and creating simple platforms. The idea was to help hobbyists and students start using CDT for building embedded applications. We have the remote download and launcher (using RSE) and gnu cross compiler support in the upcoming CDT 6.0 to help make it a real force in this area.

That work was pretty much all on hobby time. And it was fun to see it working. But I was describing that the hobby was just like work just on my own time. And my wife make a point that really hit home, “yeah, it’s like work but you don’t get paid”. Uh, yeah.

That and there are already a lot of platforms out there for hobbyists to get starting using Eclipse for embedded development. And one of those platforms has a Market place that allows you to sell the little apps that you can make. Hobby, that pays. Hmmm.

Of course, the platform I’m talking about is Android. It has a great set of Eclipse tooling for writing apps. Yes, it’s Java, and yes I bash Java regularly. But it gets the job done. And I think I have something to offer Android. Myself and a few others out on the webisphere have figured out how to build JNI libraries for Android. That gives you the best of both worlds. JDT for Java, CDT for the native libraries. You probably only need native libraries for compute intensive tasks that you can use the underlying hardware to help accelerate. But at times that is a need.

And building native libraries is pretty easy. Do a google search for Android Build System and you’ll see a general description of it and the special Android.mk file you need to provide. You need to build your library in a subdirectory under the Android source tree. But once it’s there you can create a CDT project that points to it. “make mymodule showcommands” and you’re off to the races. And CDT’s scanner discovery will even pick out the include path from the gcc/g++ commands.

Now I’m not sure how the native libraries work on real devices. It may be prohibited due to security concerns. So I’d like to try it on one before I push the idea too far. Rogers up here in Canada is finally getting Android phones in June, the same ones as T-mobile. I’ll have to invest in one and see. But going through the SDK docs, I am getting the feeling this will be pretty rewarding, in more ways than one 😉

So what does this mean for my work on Wascana, which also competes for my hobby time? I’m still keen on it, and my new strategy of “stealing” the RPM contents from Fedora will allow that to take less time. But it comes back to what I was saying in my previous blog entry. It’s a big burden trying to promote CDT for Windows development. Sometimes I feel alone and I wonder if anyone really cares. It’s a burden I’m getting tired of carrying. Hopefully someone will step up and help, or some vendor will come in and fund some of it. We’ll see.


