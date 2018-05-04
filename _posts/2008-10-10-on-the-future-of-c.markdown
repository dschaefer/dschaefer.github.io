---
layout: post
title: On the Future of C++
date: '2008-10-10 22:17:00'
---


There’s been talk for a number of years now on the decline of C++ and the rise of virtual machine and scripting language. But certainly from where I sit, the C/C++ community is still very strong. In fact, I still see many more C applications than C++, especially in the Linux and embedded worlds. Though, everyone agrees, for large applications, doing them in C++ instead of C makes sense.

But I have to admit, for desktop applications, I’m not sure C++ is the right answer like it was in the 1990’s. We’re certainly seeing Java, with the help of Eclipse, and C# on the .Net side, take a much bigger chunk of the pie chart. And I think that’s the right approach. The richness of these environments naturally enables a developer to be much more productive than in the C++ world, especially when dealing with the user via graphical interfaces. I’m pretty much ready to concede this space to those languages. Sad, but true.

But there are a few areas where I don’t think C or C++ will every go away. And that’s the areas where the developer has the need for speed and where they want to work close to and take advantage of the native processing hardware underneath their application. I often hear from people who would know, that modern Java VMs can actually do better than C/C++ in performance, thanks to run-time optimizations. But [projects like LLVM](http://llvm.org/) which provides similar optimizations to native applications, may balance the scale there. And at any rate, out of the box, native applications will start with the better performance.

When your writing a high performance application, like 3D gaming, or scientific simulations, or if your working on mobile applications where you need to balance CPU cycles versus battery life, C/C++ will always be the obvious choice. There may be exceptions to the rule, and Microsoft with .Net Compact and OSGi for Java are trying to make a splash, but C/C++ will be difficult to replace.


