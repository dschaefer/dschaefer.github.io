---
layout: post
title: A new way to get your CDT
date: '2007-06-13 13:16:00'
---


Not only am I the CDT project lead, I’m also CDT’s release engineer. That means I get to write all the cool ant scripts and stuff that pumps out the CDT builds on a semi-regular basis. Actually, I’m more the release engineer team lead and [cron](http://en.wikipedia.org/wiki/Cron) is my underling that does almost all the work. Actually cron does such a good job I hardly ever have to do any release engineering at all unless I have to change something.

Well, the past couple of weeks I’ve had to change some things. The first one is to meet [Europa’s](http://wiki.eclipse.org/index.php/Europa) guideline of having our jars digitally signed for security. That way, when you download the CDT, you know you’re getting the officially blessed version from Eclipse. I think the risks are pretty low, but it is possible for someone to make a set of zips that look like the CDT but aren’t and do something nasty things. The infrastructure created by the Eclipse team makes it easy to do the official signing so I figured why not.

The other issue we’ve been running into lately is the sheer size of the CDT builds. They passed the 400 MB mark with all 9 platforms and the two main features, runtime and sdk, that we build. With only 10 GB (now 15 GB) of disk quota at eclipse.org, we kept bumping into the limit and constantly needed to clean up builds. When you take a close look, the 9 platforms are almost identical except for the small shared libraries that we have in the cdt.core fragments. The update site, as a result, is much smaller, around 40 MB, since you don’t get that duplication.

So while I was wearing my release engineer hat anyway, I figured I’d fix all this. The recommended way to get the CDT is using our update site. We will have the runtime feature, the main one that you download, on the Europa update site. That feature along all of the others will also be on the CDT Europa update site. All this will be explained on the [CDT’s website](http://www.eclipse.org/cdt) when we release. The jar files will also be compressed using [pack200](http://en.wikipedia.org/wiki/Pack200) to make downloads a lot faster and save bandwidth on the Eclipse servers and mirrors.

The other big change is that we will no longer be releasing feature and platform specific zip and tar.gz files. Instead, we will have a single zip file called the CDT Master that is an Archived Update Site. So you can install normally via our update site on Eclipse.org, or you can download this zip and install it, still using the update manager, but from the zip file instead. We are currently doing our nightly builds this way, and it works well.

This will hopefully make the CDT easier to get up and running while saving a lot of space and bandwidth for Eclipse. It’s good all around, but it is a change and, as always, I’d like to hear your feedback on it.


