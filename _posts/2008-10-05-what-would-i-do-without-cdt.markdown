---
layout: post
title: What would I do without CDT
date: '2008-10-05 12:20:00'
---


While waiting for my VOBs to sync from Salburg to Ottawa, I thought I’d poke around qemu to figure out exactly what I would need to do to add a PCI device. Apparently, there’s very little, if any, documentation on how to do that. And I even saw one response to a similar query that told the guy to go look at the source. So I did.

I started by grabing the source for the latest qemu release 0.9.1. I created a CDT Makefile project and untared the release into the project directory. I created an External Tool to run configure with the options I wanted and then I did a project build which ran the resulting makefiles. So far so good. Looking at the Includes folder on the project, I see it caught the mingw gcc standard headers as well as my project as an include path.

So off I went. First I looked for things beginning with pc_ in the Open Element dialog (Shift-Ctrl-t). There I found the pc init code and went looking there for PCI devices. I found the LSI SCSI device init and hit F3 to go look at the implementation. There I started seeing some generic PCI type things. To see what other PCI devices I could look at, I selected the call to register a PCI I/O region and did a search for references. In the Search results view I quickly saw other PCI devices – VGA displays, the IDE device, some networking things, USB. All good examples.

It wasn’t long before I figured out what I needed to do. It got me thinking. How did I ever do this before the CDT and how are the poor guys still stuck in the command line world doing stuff like this. I guess I used to do the same thing but used grep which does simple text searches. But there’s no way I could do the same navigation with the same speed. And things like Alt left and right arrow to go back and forth along my path doesn’t happen in that environment.

No, CDT rocks. I hear a lot lately about how there are still many people hesitant to leave the safety and comfort of the command line world. I think that’s too bad. They’re missing out on some real productivity gains.


