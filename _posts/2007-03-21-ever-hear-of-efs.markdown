---
layout: post
title: Ever hear of EFS?
date: '2007-03-21 21:43:00'
---


We’re at a critical juncture in the evolution of the CDT. Everything has been going so good lately, with tons of indexer and build improvements, that I guess we were due for a bit of a crisis. The issue we are grappling with is how to use the CDT with projects that have source files sitting on a remote server, possibly across the Internet somewhere. It’s a tough environment that will definitely stretch Eclipse and the CDT if we are ever successful in making it work well.

The solution I’ve been hoping to push is to use EFS to access those files and, in theory, the CDT should just work. What’s EFS? Well, it’s the [Eclipse File System](http://wiki.eclipse.org/index.php/EFS), which provides a layer of abstraction at the same level as java.io.File, but allows different implementations. Using the right IResource APIs and URIs instead of IPath, and everything should work. It seems designed to meet our needs.

I managed to build a FileSystem using FTPClient from Apache’s common.net. My test is to run it against the ftp server on the CDT build machine at Eclipse. Saving files is a bit slow, and I guess that’s to be expected and we can probably introduce some caching and worker threads to at least get it off the UI thread. I imagine [RSE](http://wiki.eclipse.org/index.php/TM_and_RSE_FAQ) does this already and will need to take a closer look at their EFS implementation to see if it would work better.

The bigger issue is the number of instances where plug-ins are assuming IPath works and IResource.getLocation() works. And I kind of knew that going into it, that we’d have some work in the CDT to solve this, and that proved to be true. So I tried a General project and text files worked fine. So I though I’d try something more involved. How about a Ant build.xml file. Well, there again, massive NPEs because the build.xml editor and the AntModel assumes IPath to work. Not only that, they use java.io.File to get at the file. Ouch.

It is pretty clear that little work has been done to try out a real EFS implementation as backing for IResources, or at least not enough work. My feeling is that this remote project idea must transcend the CDT, and we’ve even thought about starting a new Eclipse project to focus on it. It’s clear there is a lot of work to do and we need to start organizing if we really want to make EFS remote projects work.


