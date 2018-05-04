---
layout: post
title: Cross Compiling Fun for EclipseCon
date: '2008-11-06 22:23:00'
---


It’s been a busy couple of weeks for me as we get our commercial Eclipse p2-based installer into product testing. It’s looking good but there’s always those last minute fires (i.e. bugs) to fight.

In the background I’ve been trying to set up an environment that will allow me to use the CDT to build Linux applications from my Windows box, and then run and debug those applications on a customized version of the Qemu emulator that is also built using the CDT. Once I get this environment together, I plan on presenting how to do it at EclipseCon as either a tutorial or long talk. It’s a great demonstration on how well the CDT works for multi-platform development.

My first step was to put together a cross compiler. The gcc compiler suite is great at it, but it’s not obvious how to do it on Windows. Most GNU packages are hard to build on Windows, even with the MSYS environment from the MinGW gang, or Cygwin.

I first tried with MSYS. I copied over the C library headers and libraries and then tried to build binutils to get the assembler and linker, and gcc itself for C and C++. [I was generally following the instructions here](http://www.linuxquestions.org/questions/linux-software-2/free-compilers-and-cross-compilers-for-linux-and-windows.-640030/). I got really close, but unfortunately I ended up with a linker error when creating the gcc compiler support library (libgcc). Grrr.

Thinking about my reference article a little more, I remembered that even the MinGW developers build MinGW on Linux. I then discovered that the Linux distribution I am using (Debian lenny) already has the MinGW cross-compiler and libraries as a package. So I installed that and I suddenly had the ability to build Windows executables on Linux. So given that, I built binutils and gcc on Linux so that it would run on Windows to build executables for Linux. Wow. That’s quite a few levels of indirection. But it worked!

Now all I need to do is build a CDT integration that puts the i686-linux-gnu- prefix on gcc and puts the location of the tools in the PATH and I’m ready to build Linux apps from my Windows laptop.

I’m looking forward to showing this off at EclipseCon. It’s talks like this that show practical uses of the CDT and extensions people can build for it that we really need to highlight to the community at EclipseCon. Mine is only one, we need a few more. So if you have an idea, feel free to go to [the EclipseCon site](http://www.eclipsecon.org/2009/) and submit a proposal.


