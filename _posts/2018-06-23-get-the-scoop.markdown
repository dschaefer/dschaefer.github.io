---
layout: post
title: Get the Scoop, a Homebrew for Windows
author: Doug Schaefer
tags:
- eclipse
---
# Get the Scoop, a Homebrew for Windows

When I came back to QNX over six years ago (wow, it's been that long?), they offered a choice of one of the the three main environments. I was excited to see what all the hype was about and picked Mac. I really enjoyed it. It provided a great blend of user experience with the power of Unix and the shell underneath. The trackpad on the MBP is amazing. It's under rated how much a productivity enhancer that is.

But eventually that machine got old and beat up and it was time for a new one. I had my fun with the Mac, but it's not what's used by many of the users of the tools I build. In the embedded space you see a pretty solid mix of Windows and Linux. And I was interested to see how much better Windows 10 was and whether it could overcome it's really crappy command line environment. So that's where I went.

I knew Eclipse works well there. It was invented there and still looks like a big MFC app. But selecting a shell environment revealed a lot of choice.

* [MSYS](http://mingw.org). This was the environment I used the last time I was on Windows. It came as the shell for the MinGW toolchain. But it seems to have died.
* [CYGWIN](http://cygwin.org). This environment bugs me a lot as it maps Windows paths to Unix paths and confuses the hell out of native tools, like Eclipse CDT.
* [MSYS2](http://msys2.org). This is a pretty rich environment that seems to be an evolution of the old MSYS. It comes with a package manager but the choice of Arch Linux's pacman is a tough one. It makes it your responsibility to figure out what 32/64-bit host and target combinations of the toolchains and libraries you want to install. But it does have everything, even Qt.
* [Scoop](http://scoop.sh). Scoop is a more general package manager and is pretty easy to use. It's very active and has a good community keeping the tools up to date. And while it has all my favorite tools for building C/C++ apps, it doesn't have any libraries. But that's fine, you should be building those yourself anyway to make sure you're using the same toolchain settings.
* [Chocolatey](http://chocolatey.org). This is another package manager but at a higher level than Scoop. It's less focused on being a shell and assumes you're a Powershell user, which I'm not and barely understand.
* [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10). Also know as Bash for Windows, it provide a Linux emulation layer and gives you access to real Linux distributions. You can use it to access you're files outside of it's Linux emulated file system, but it's pretty weird and not everything works.

For now, I've gone with Scoop. I really like it because I also use it to install other tools I use like docker and kubectl for my test cluster, and maven and python and svn, pretty much any command line tool I need. And it manages the PATH for you so all the tools are available in native apps without any magic, including the Windows command line if you're stuck for anything else. But most of the time, I use busybox which gives me all the Unix tools I need including a not quite bash compatible shell, but that's fine. I do wish it had C/C++ libraries like SDL or Qt, but it is open source and extensible so I could just do this myself.

The good news is that I'm finding myself very productive on Windows. I have a great shell environment with Scoop, good editors with emacs and Visual Studio Code, and Eclipse which still works best on Windows, and all the Windows apps I need. I don't miss my Mac at all.