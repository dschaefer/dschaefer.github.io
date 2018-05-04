---
layout: post
title: Can old NeWS be new again?
date: '2008-06-03 23:19:00'
---


I’m going to really show my age here. Back when I was doing my Masters degree at the University of Saskatchewan (now there’s a Canadian word that’s hard to say even for Canadians), I was doing graphical representations of software models. Yes, my modeling roots go back 20 years. Essentially, I was trying to come up with a generalized diagramming model that could represent different modeling languages.

When it came time to do the prototype, I had a choice of windowing systems that ran on our Sun and HP boxes we had in the lab. Of course, we had X Windows, X11R2 if I remember correctly which was much better than X10.

We also had this new system from Sun called the Network extensible Window System. It was wacky but very cool and had a wacky and cool acronym, NeWS. Essentially you programmed the window server using PostScript (of all things) that was extended by Sun to handle windowing and input devices and asynchronous communication back to the client. It was quite bizarre to be writing PostScript code to do UI but it was a good way to separate UI from Core with an efficient protocol you got to create yourself to best suite the application.

Unfortunately, the implementation was very slow and awkward and the co-operative multi-tasking made it impossible to debug endless loops (but it did help me learn the Sun equivalent of Ctrl-Alt-Dlt). I eventually picked X Windows and this wacky new language called C++ and the rest is, well, even more history.

What NeWS reminds me of today is this whole concept of Web 2.0, and Flash/Flex in particular. And not because PostScript and ActionScript have the same suffix, but because the architecture is very familiar. And it made me wonder if we could use it in the same way, as a windowing system. I can’t remember how I programmed the C side but if we used a similar API and protocol would it be any good? Now if I can only find some 20 year old documentation to find out.


