---
layout: post
title: Forget OO, C++ is a better C
date: '2007-05-15 09:33:00'
---


I was working on [bug 176353](https://bugs.eclipse.org/bugs/show_bug.cgi?id=176353) trying to get interrupt signals sent to cygwin-based gdbs. Part of the magic for that in the CDT is something called the Spawner. Spawner subclasses Java’s Process and adds the ability to send Unix type signals to them. It also implements some fancy I/O but that isn’t supported on Windows. This class is a little Java and a lot JNI native code that interacts with the operating system to implement the signals as well as the other Process type things like starting up and waiting for completion of the process.

So, I guess this code was written originally with Visual Studio 6 many moons ago. However, continuing with my theme of using MinGW for Windows development, I’ve created makefiles to build the spawner DLL. What made this situation a little weird was that the original creators of the spawner were guys who didn’t really know C++, so they did it in C. I always find it weird doing C in VS, but that’s what these guys did. So when I wrote the makefile, I used make’s default of running gcc on these files. Makes sense.

However, I was having trouble when I added a calls to a couple of Windows routines. I was getting undefined references at link time to the two calls I added. Weird, I didn’t get any compile errors. When that happens it usually means I forgot to add the library. So I added it and still got the errors. What’s going on here? Is it something broken in the MinGW port of these libraries? Was my code just getting tired and cranky?

Well for some reason, maybe I was getting tired and cranky, I wondered if it was because I was using C instead of C++. Part of my debugging technique is to start assuming the least likely cause and testing it out. This was really damn unlikely. But I tried it out. I changed the compiler to be g++ and ran it over the .c files. I thought it would have treated them as C files and nothing would really be different.

But to my surprise, g++ compiled the .c files as C++. And I got a ton of errors. And almost all the errors were for passing the wrong types to functions, especially since I was using UNICODE and not everything was really using wchar_t. Well, no wonder things weren’t working. Of course the one thing it found were compile errors with the two functions I was calling. I had forgot to add the include to the header that defined them which specified the correct calling convention, WINAPI, which is why I was getting the link errors in C. But then C was happy to play along without having to see the declarations of the functions and made some bad assumptions. I wasted a good couple of hours trying to figure out what was wrong.

So, forget the object-oriented, templates, namespaces, operator overloading, and all the other cool features of C++, C++ at its core is just a much better C. It has proper type checking that helps you find those errors before link time, or worse, run time. It all feeds into helping you build better software faster, which is what this whole tools industry is all about. And if you’ve programmed in C++ for years and have to go back to C, don’t forget to make that paradigm shift back to the 80’s…


