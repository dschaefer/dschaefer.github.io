---
layout: post
title: CDT 6.0 M5 is Available, BTW
date: '2009-02-22 15:55:00'
---


I’ve been “nose to the grindstone” since the holiday break getting our Wind River Installer out the door, twice. But the good news is that the CDT contributors have been very busy working on CDT 6.0 while I wasn’t looking very hard. I have been waiting for the C/C++ IDE Package for M5 to be built. In the meantime, we do have the bits up on the CDT Galileo update site for you to try. Just download the [Eclipse Platform or SDK 3.5M5](http://download.eclipse.org/eclipse/downloads/drops/S-3.5M5-200902021535/index.php) and add the following URL as an update site:

http://download.eclipse.org/tools/cdt/releases/galileo

Most people will want the “Tools” feature in the “Main” group, which will give you everything you need to work with the gnu toolchain. And yes, the features say 5.1.0, but we’re tricking the API tooling with that to keep track of API changes. We’ll be 6.0 when we go out the door in June.

I’ve actually been using CDT 6 for some technical investigations I’ve been doing lately, the qemu source being one of them. One of the biggest issues with the CDT that we’ve been fighting forever has been taking projects that have been developed without an IDE, that don’t have any real structure to them, bringing them into the CDT, and having our indexer parse and create useful search information for them. And this is especially bad if we can’t figure out the include paths to find the header files needed to parse properly.

One common pattern we have noticed with the include path was where all the user specified include paths were actually folders in the workspace. Everything else came from the built-in include path. At the very least, if we could search the workspace when looking for header files that were unresolved, we could probably resolve them.

Well in CDT 6.0M5, that functionality if finally there (thanks, Markus!) and it works superbly! Many of the unresolved headers I saw in this one project I was looking at, which targeted many different OS’s, were magically resolved, and features like Open Definition (F3) worked great. Sure, if you have multiple header files with the same name in your project, we may pick the wrong one to resolve, and there will still be issues if you don’t specify external include paths, but it’s huge step forward for CDT usability.

There are other interesting things in M5, including the Debug Services Framework which has moved from the Device Debugging project to the CDT and should become our “official” debug framework over time. You’ll notice the major issue we have with having two debug frameworks when you go to launch (double the launch configs 🙁 ), but we are working on a solution to that.

We’re still making great improvements to the CDT as we go. Most of them are under the hood as the feature set we have is working quite well already. And there are still things to clean up, like our managed build system and the underlying build model and the need to integrate that with our debug models. But I know I’m a happy CDT customer myself, and I hope you get a chance to try out CDT 6.0 M5 and give us your feedback.


