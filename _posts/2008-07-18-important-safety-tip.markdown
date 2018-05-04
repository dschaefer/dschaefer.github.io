---
layout: post
title: Important safety tip
date: '2008-07-18 14:49:00'
---


So when you go to redefine the key sequence in Eclipse to do ‘Build All’ make sure you’re hitting the Ctrl key and not the Shift key. It explained why I couldn’t define the CXXFLAGS macro in my Makefile. Instead of Ctrl-X Ctrl-M for build all, I had accidentally defined it as Shift-X Shift-M. Weird (that it let me), Cool (that I could do it), but took me a little while to figure out that’s what it was and not something wrong with my keyboard when Shift-X didn’t do anything 🙂

BTW, thanks out to the guys who are contributing to the Emacs key bindings. I’m loving it! All I need to add is this Build key sequence, which Emacs doesn’t define either anyway.


