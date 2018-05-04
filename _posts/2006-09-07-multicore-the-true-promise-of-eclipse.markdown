---
layout: post
title: 'MultiCore: The True Promise of Eclipse'
date: '2006-09-07 18:41:00'
---


So, I needed a board to help try out some JTAG things (for those readers not involved with embedded development, a board is a little computer kind-a thing). We had just received an OMAP board which uses a TI chip that contains both an ARM general purpose processor as well as a TI DSP (digital signal processor). Of course, my focus was on the ARM processor that runs our operating system and it was pretty cool to getting it up and running with little effort.

But after a while, I started wondering what people use this board for. I’ve been away from embedded development for a few years and man have things changed while I was away. I soon discovered that the main use of this thing is for audio processing. There are some audio jacks as well as a connector to plug in an LCD screen. By programming some audio processing algorithms into the DSP, you could make a pretty cool multimedia device with this thing.

My curiosity then wondered over to how one would program the DSP. If I had a compiler with an integration with the CDT and a debugger that understood how to debug the DSP and that was also integrated with the CDT, then I’d then have a complete multi-core development solution where I could have regular software projects and DSP projects and work on them all at the same time.

It’s a very interesting time in the embedded industry with the multi-core phonmenun. I think we’ll see a lot of new processors come out that have specialized parts. What I hope to see, and I’m pretty sure it will happen, is different vendors working together integrating their Eclipse-based technologies and unify their development activities into a single workflow for the developer who sees these boards as a single target. That is the true promise of Eclipse!


