---
layout: post
title: 'CDT Summit Report: What to do about the Eclipse Platform'
date: '2010-09-28 15:05:00'
---


We had a lot of heated debate about what to do with the Eclipse Platform and the troubles we’ve had trying to contribute to it to allow it to meet the needs of our customers. There have been some successes, there is no doubt. We have flexible resources in 3.6. We have flexible debug in the platform for quite a while now. So we are very thankful for that.

But we’re still not in a good place yet. We’re still really struggling with build. CDT builds are complex beasts involving external compilers and linkers and other utilities and generators. Builds tend to take a long time. My standard sized C++ project porting the Irrlicht game engine to Android takes about a few minutes to do a full build with a Minimum 3-5 seconds for a one line change. It’s not “instantaneous” like Java and dynamic language builds tend to be. So features like automatic builds never made sense for us.

Also, our builds tend to be managed by external tools, ‘make’ in particular, that manage the “delta” of what needs to be built for us. The resource delta that the platform provides is useless in those cases, other than as an indication that something has changed and we need to invoke make. Mind you we tend to always build anyway just in case we have external files that may change that aren’t being tracked by Eclipse.

That leads to the oddest workflow, clean, which in the C++ IDE’s we’ve used in the past, means just that. Remove all previous build output. But since that also clears out the Eclipse build state, it invokes a FULL_BUILD right away to rebuild it, which we then interpret as the need to call out to make which then puts the build output right back. And if we ignore FULL_BUILDS, we miss the initial build. It’s a mess.

The good news is that we have people working on fixing these things, and have opened bugs against the platform and attached patches to them. But it’s been really slow to get them looked at or they are being rejected outright. What ends up happening is that vendors fork the platform and apply the patches they need anyway. Now that’s not a healthy situation when we are trying to build an ecosystem when everyone has a different eclipse platform you need to plug into.

So what do we do about this? Is e4 the answer? No. In fact surveying the crowd at the CDT summit, no one was interested in the features that e4 brings to the table. It doesn’t address the problems that we as a C++ IDE community have today. And we need to those things fixed in the Platform today, not in an incubator. Fancy UI frameworks are maybe something we need down the road, but our customers want us to get the basic workflows working well first.

So in a drunken stupor (well stupor anyway) at our celebration event I threw out a proposal to the people standing around me and then to others during the week. e4 is a fork of the platform. It was created to try out some new ideas. Why don’t we create our own fork of the Platform focused on meeting the needs of the CDT community and for our fellow Tools projects that have the same needs. That way we can at least share the forks we’ve already created for our products. We still need to run all the same plug-ins we do today such as Mylyn, JDT, etc. So we can’t go crazy and change the world. But at least we’d have control over it to make sure it meets our needs.

You know me by now. I like to brainstorm with the community. So I’m only semi-serious about forking the Platform. We are taking a serious stance on the bugs we have opened up there and I hope the Platform team will work with us for the mutual benefit of our users. We are frustrated about the lack of progress and we do need to think of alternatives. And forking the Platform isn’t as far fetched as it once seemed. It’s actually a admission of what many in our community are already doing.


