---
layout: post
title: Going with the data-flow
date: '2008-07-27 21:56:00'
---


I’ve just been reading articles in Wikipedia on [dataflow programming](http://en.wikipedia.org/wiki/Dataflow_programming). This programming paradigm captures what I think is the greatest need we face to built the multi-threaded applications of the future. It also explains where a lot of the concepts in UML Actions and Activities come from.

From what I understand most of the dataflow languages are visual languages. The [SynthMaker](http://synthmaker.co.uk/index.html) tool that came with my [Fruity Loops](http://www.flstudio.com/) is like that. The page also lists the hardware description languages, Verilog and VHDL, in this category. I think they’ve left out SystemC since it fits into that mould as well.

But even if dataflow programming is the big new paradigm, I firmly believe that any new paradigm will only be mainstream if it’s familiar to developers. There’s been some great programming languages over the years that you would swear are much better than C (Ada comes to mind, Pascal was really good too), but if you look at the most popular languages in use today, C-like languages, and C++, Java, and C# in particular, win by a land slide.

So it comes back to [what I was mentioning earlier](http://cdtdoug.blogspot.com/2008/07/lesson-on-systemc.html). SystemC is a great example of a C++ library and run-time that implement a different programming paradigm but let you reuse all the skills you’ve learned with other C++ applications. And, it’s an example of a language that supports dataflow programming which we need for massively multiprocessing applications. It’s definitely a source of inspiration.


