---
layout: post
title: Smartphones, Smartbooks different by necessity?
date: '2009-06-16 14:04:00'
---


Boy I’m having fun with Android. Maybe because it’s the first time I’m getting the chance (albeit in my spare time) to do some real embedded development. And even in the playing I’m doing, I am experiencing the challenges that regular embedded developers face. Yes, believe or not, even with the latest and greatest hardware, you are limited by the amount of memory and storage your device has, and by the speed and capabilities of the processor. Not to mention power (feel like running your graphics loop at full speed, see how long your battery lasts doing that). You really have to think about these things and write your code carefully to be successful. (And I won’t get started on Java again).

One thing you still see in the rumoursphere with Android is the spreading of it’s wings into the “smartbook” world. I love that term, Smartbook. Mobile Internet Device is too vague and I think there is a clear delineation between the tree contenders: smartphone, startbook, netbook. Smartphones are the small handheld things we know and love today. Netbooks are the small notebooks which likely have a hard drive in them. But Smartbooks are an exciting middle ground between the two. They have usable screens, 5-9 inches, but everything else is like a smartphone, particularly in mobility and power consumption. A good smartbook should last the day without charging making it handy for carrying around conferences like EclipseCon, for example :).

I’m not sure Android can scale to the big screen, so I’ve been looking around at the alternatives and Moblin in particular. I can see myself becoming a big fan of Moblin development. It’s much more like a traditional Linux environment and has my favourite packages available, including Qt, GTK, and X/OpenGL. But I wonder if Moblin has scalability issues the otherway. All those great packages take a lot of resources and they certainly won’t fit on the 256MB NAND flash chip on my Dream phone. And I don’t see consumers being happy losing even more battery life to support bigger and faster chips. So in the grand scheme of things, it appears to me that it requires us to have different software platforms to match the hardware. But we’ll see if the Moblin guys manage to get running on a smartphone.

That’s lead me to wonder if the same is true with the applications. It’s pretty obvious that smartphone and desktop apps have to be different. Screen size and the rest of the resource constraints on phones force you to design the app differently. Now is the same true for Smartbooks? Is this a third category? I have a feeling yes. You may have a bigger screen size and it may look like notebook, but the resource constraints are still there. You still need to be worried about power consumption and you won’t have a desktop class processor to get you out of trouble with sloppy algorithms. Mind you, that’s just good development practice anyway. I’ll have to think about this a bit more.

At the very least, you have a different development environment for your smartbook apps. Generally you’d have a cross compiler, even if it is the same processor. It helps keep the environments separate from the rest of your development desktop. Mind you Moblin seems to be going to great lengths to avoid that for some reason using VMs and remote builds. Cross compilers aren’t that scary, you know :). And the CDT does a great job working with them.


