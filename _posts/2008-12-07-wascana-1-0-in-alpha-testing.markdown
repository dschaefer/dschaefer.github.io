---
layout: post
title: Wascana 1.0 in Alpha Testing
date: '2008-12-07 16:33:00'
---


Well, that didn’t take very long. I’ve spent a few hours building my special p2 artifact repository that manages installed files, including extracting them from an archive and deleting at uninstall time, along with it’s associated p2 touchpoint that hooks it all up. It’s not a lot of code and you can see it in CDT’s CVS space (repo: /cvsroot/tools, module: org.eclipse.cdt/p2).

I’ve also created a generator that creates p2 repositories that use that touchpoint to install remote artifacts from various locations, mostly on SourceForge. Currently I only have support for the MinGW toolchain and the MSYS shell environment. I’ll add libraries as I build them with the 4.2.3 compiler I’m using here. I’ll start with SDL and also do wxWidgets and boost. We can always add more later.

It’s working very well. Managed build picks up the mingw toolchain and uses it when you select the MinGW toolchain. MSYS doesn’t work yet for Makefile projects but managed is usable now. And here’s how:

1. Unzip the [Eclipse IDE for C/C++ Developers](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/ganymede/SR1/eclipse-cpp-ganymede-SR1-win32.zip) anywhere you’d like on your machine. You can also start with any other Eclipse install as long as you have the CDT installed.
3. In Software Updates, expand out the tools/cdt/releases/ganymede site into CDT Optional Features and install the Eclipse CDT p2 Toolchain Installer feature. Allow Eclipse to restart to make sure things are initialized (I’m not sure if you really have to do this, I’m just paranoid).
5. Go back to Software Updates and add the Wascana repo site at http://wascana.sourceforge.net/repo. Install everything under the MinGW Toolchain category. This time you don’t need to restart. You don’t even need to apply changes.

Once you’re done, you can go to the directory containing eclipse.exe and you’ll see the mingw and msys directories there, ready to go. Well at least the mingw dir is, I still need to set up msys correctly to find the mingw compilers, but it is only an alpha :).

Feel free to give it a try and let me know what you think. I’m pretty excited with how this is going. While creating this, a new version of the win32 API component came out and I added it to the repo and the Update… feature found and installed it. Very cool!

It’s a very interesting path where this is going. The ability to incrementally add in libraries and update new versions of the components will be a great showcase on how p2 can manage more than just bundles. Not to mention help me build one heck of a Windows development environment based on the CDT and open source tools and libraries.


