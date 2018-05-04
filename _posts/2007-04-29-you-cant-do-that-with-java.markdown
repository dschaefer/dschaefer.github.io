---
layout: post
title: You can't do that with Java
date: '2007-04-29 20:12:00'
---


O.K., [it’s not that I hate Java](http://cdtdoug.blogspot.com/2007/04/f3-cdt-wunder-key.html). It’s more, I run into times where I need to do something that I can’t do in Java. Some of my favorite C++ features include operator overloading, crazy C++ templates like the ones you get with the Standard Template Library, and flexible memory management, not to mention the great job that C++ compilers do at optimizing all this magic into fast object code.

It’s really the flexible memory management that I miss the most. Allocating memory out of the heap is expensive. That’s pretty common knowledge. With Java, every Object gets allocated out of the heap. I remember the first time I ran into this early in my Java career. I had this little class that had a couple of fields that I used to store temporary information that got passed down to some other methods. I couldn’t believe that I had to allocate it out of the heap. With C++ it had become second nature to declare an object and have it automatically allocated on the stack. And when the function I declared it in finished, whether due to a return or an exception, the destructor for the object gets called so you can clean up any mess. And using C++ pass by reference, I was able to do all that with minimal typing (my other mantra – I hate typing, especially with my sore finger right now).

The other cool feature of C++ is the ability to override the operator new to do your own memory management. That way you can allocate all instances of a class in a special memory pool. Or pass parameters to operator new to do anything you want. I’ve run into this as I’ve started looking closer at ray tracing algorithms (my new hobby). One of the speed ups they mentioned was allocating all contents of one of the structures in a given memory region to help leverage CPU data caches in an effort to squeeze every ounce of performance out of the machine as they can (which is really needed to get any resemblance of real-time ray tracing on today’s machines). Now that’s something you can’t do in Java, at least not without some native code, which then isn’t really Java.

Java has it’s place and I love it for writing Eclipse plug-ins. But despite bold predictions by the IT industry, C/C++ will never go away as long as we continue to throw as much processing at these fancy new CPUs and GPUs as we are. For some reason, our appetite for speed continues to outstrip all that performance that the silicon vendors are working so hard to put in our hands.


