---
layout: post
title: Fitting Eclipse into my world
date: '2010-07-19 14:38:00'
---


As I blogged a few days ago, I’ve started working on a game engine using open source bits. Part of it is just to satisfy my hunger to learn more about game development, but the more practical benefit of this effort is to better understand the plight of the C/C++ developer using the CDT on a real and fairly sizable project.

And I have my first lesson. It came about thanks to git. I have the source checked into a git repository out on github. Now, since the root of the game engine is open source libraries, I was working in the command line to extract them into the git repository. As a result I got used to using git from the command line, including adding a .gitignore so that git wouldn’t check in my Eclipse .metadata directory and any directories containing build output.

I then started setting up the projects as CDT projects and started working in Eclipse. And I gave the Helios egit plug-ins a try. Unfortunately, they currently don’t support .gitignore and as a result I got weird results that caused me to lose trust in egit, like ?’s on the folders I have listed in my .gitignore. Or did I forget to add them there? Not sure. I have to go back to the command line to look. At any rate, I ended up staying there and now I just use git from the command line. At least until egit 0.9 comes out with .gitignore support and I’ll try again.

But this article isn’t about egit. It’s about Eclipse and how developers who do C/C++, especially experienced ones, work. The command line and command line tools are still a very important part of the development cycle and Eclipse and the CDT need to deal with that.

I see a lot of functionality in Eclipse assuming that projects are the root of your life. Well, it’s not in my case. I have a git repo which contains directories that contain projects and there are some that do not. There’s even a README file at the root and some files to help me build for Android using CMake.

I think there’s a concept missing in Eclipse. We can equate the root of my git repo as a workspace. But then there are things in that workspace, files and folders, that aren’t projects. I would like to be able to browse them, and maybe even edit the files, without having to go to the file explorer. Essentially I need a file navigator rooted at the workspace. I’m not sure whether we need a separate view for that, or to just allow Workspace roots to have IFiles and IFolders and make them navigable in the project navigator.

I’d like to hear other people’s experiences, especially those who try to mix Eclipse with command line development. Is this something that would be useful? Are there other things?


