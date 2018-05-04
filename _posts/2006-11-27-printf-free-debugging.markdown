---
layout: post
title: printf-free Debugging
date: '2006-11-27 11:33:00'
---


When people ask me who the CDT’s biggest competitor is, they often expect me to say things like VisualStudio or one of the many Linux IDEs (and no, Netbeans isn’t quite there yet). But the truth is that the biggest competitor to the CDT remains good ol’ vi and make (or emacs and make for the more advanced developer). We are certainly working hard to make the CDT an easier environment to adopt, but there are still the masses that can not afford the time to climb the learning curve.

But the ‘vi and make’ answer addresses edit and build. As I’ve mentioned here before, my favorite IDE feature remains visual debugging. For me, nothing beats that quick glance at the stack and then moving over to the variables view to see what all their values are. Measure that against the number of gdb commands you’d have to enter to do the same, you just can’t beat it (did I also mention that I hate typing?).

But looking around the industry, I finally figured out who our main competitor on the debug side is, good ol’ printf. Now in some environments where it’s hard to set up a debugger and all you got is console output, you have no choice. But how do these guys live with the edit/build/debug cycle every time they want to see a different variable output? And we’ve all done it at some point in our careers and likely very recently too. We need to make sure we have the right tools to put a stop to this.

At the very least, for the embedded developer, you have JTAG to drive things at the lowest level. And with many of the JTAG devices now supporting the GDB remote protocol, you can use gdb to debug at these levels. The next step is to see the CDT better support GDB running in that configuration. And that’s what I’m working on today (sorry Windows debugger, you’ll have to wait a couple of weeks).

Tools have an immense opportunity to improve developer productivity. But in order for the developer to benefit from this, the tools need to be easy to learn and use. I think that’ll be the next big challenge for the CDT, and one we’ll need to address to be truly ‘Uber’.


