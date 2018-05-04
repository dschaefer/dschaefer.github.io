---
layout: post
title: Unexpected surprise in my Fruity Loops
date: '2008-03-30 09:45:00'
---


As I mentioned previously here, I am starting to get into making my own electronic music. I’ve played guitar for many years as a hobby (and I’m nowhere near as good as [Steve Northover](http://4.bp.blogspot.com/_H4Kr0LHNMcQ/RfEGAJa4XwI/AAAAAAAAAHY/8VXI-t8jwzM/s1600-h/Steve.JPG)) but wanted something that I could play with on the road (yes, I was creating music on my flight down and back to EclipseCon). That and it gave me a way to mix hobby and work since I could build software synthesizers using the CDT and Wascana.

I purchased a copy of FL Studio, which has been previously known as Fruity Loops when I first heard about it a few years ago. It’s a goofy name you’d associate with a kids product, but it’s now a full fledged digital audio workstation and deserves a grown up name. They just came out with a new version and one of the hidden gems is the inclusion of a [product called SynthMaker](http://synthmaker.co.uk/) that lets you build your own software synths using a visual programming environment.

O.K. creating your own synths without having to write C++ code. I guess not all musicians know C++ so I get it. And creating them visually is an interesting approach that newbies should be able to figure out.

But what struck me as I started digging into the sample synths it ships with (which sound awesome BTW) was exactly how powerful a programming environment this is. You create modules which have built in algorithms for everything from audio processing to IO handling to the rendering of the graphics for the synth UI. And then you hook them all up using interface ports and data flow lines.

OMG (the pun is unintended but now that I look at it, it’s pretty funny), this is UML Action Semantics in action! Ever since I was involved in the review process for action semantics (including a very awkward call with Jim Rumbaugh – man, was I intimidated by the legend!), I had a vision of a visual programming language based on the concepts. You essentially declare objects and actions that you perform on those objects and link the actions together with data flows and control flows. And now that multi-core computing is becoming all the rage, I figure it’s even more important. I think it’s the only way programmers will be able to grasp multi-threaded programming, by forcing the code to flow in multiple dimensions instead of the single dimension text streams we have today.

So while I’m taken aback that I found this vision manifested in such a niche product, it helps me realize that this vision could be practical. I can’t wait to start diving into it further and getting real experience at programming this way. If it works well, then I can really see the need to manifest this as a general language. And wouldn’t this look great written using the Eclipse Modeling projects.


