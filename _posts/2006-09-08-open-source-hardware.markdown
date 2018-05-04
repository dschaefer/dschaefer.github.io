---
layout: post
title: Open Source Hardware
date: '2006-09-08 09:13:00'
---


I’m sure I’ve told this story before somewhere, but I used to sit across from an ASIC designer many years ago. This is when I first started using ObjecTime Developer for software modeling back in the early 90’s, a couple of years before I joined the company. He was marveling at how we software designers had started using graphical tools, just as ASIC designers were abandoning similar tools for textual description languages. I’m not sure why they made that transition, but given the complexity of the chips they were designing, my bet is that the graphics didn’t scale well for them and the tools back in the early 90’s weren’t very good – no Eclipse back then!

This guy was coding in a hardware description language called Verilog. I peaked over his shoulder one day and saw that it looked a lot like C code. I found that very interesting but it took many years before I sat down and took the time to learn a bit more about the language and what it could do (there wasn’t much of an Internet back then either). It indeed was C-like and was structured a lot like C, and I’m sure suffers the same scalability issues that programming in C can sometimes cause. Thankfully, there is an [Eclipse plug-in](http://veditor.sourceforge.net/) to help you write your own Verilog code.

Fast forward to the recent future and my interest in MultiCore processing, I found it quite interesting when Sun announced that they were open sourcing their Niagara line of processors. Diving deeper, I was able to find the Verilog code for their T1 chip published on [www.opensparc.org](http://www.opensparc.org/). Other than being cool to look at and maybe interesting for students to learn CPU design with, I didn’t really see the benefits of open sourcing a CPU design.

Then yesterday, I ran across an announcement from [Simply RISC](http://www.srisc.com/) that their engineers had taken the open source T1 code and made a simple SPARC embedded processor out of it. Of course with the T1 source being GPLed, they have released the source for their CPU as well. Is this the start of something? I’m still a bit doubtful. Chip companies make most of their money on the designs they come up with, not necessarily the chips themselves. But it is an interesting phenomenum to watch out for.


