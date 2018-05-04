---
layout: post
title: Fun with RSE
date: '2008-10-19 22:24:00'
---


I love my home office setup. I still have an @work office that I go to, but with an Autistic son who’s home schooled, I never know when I need to work at home for a day or two so it’s good to have something setup so I can continue working when I do. In the office, I have a TV which I’m using to watch the great baseball playoffs happening right now and I’ll watch hockey whenever I get the chance too. And while doing that, I get to play on my laptop, like writing here in this blog.

At any rate, tonight I thought I’d try hooking together the virtual machines running in my Windows environment. One is qemu running my simulated OpenConsole thing to which I’ll be adding OpenGL support. The other is VirtualBox running a desktop version running the same distro, i.e. Debian, where I’ll be building the device driver and app prototypes. VirtualBox has nicer desktop control than plain qemu.

The question comes: how do I get the stuff I’m building on the dev machine to the target. I thought of NFS, which is probably the best choice, but I’d need to spend time figuring out how to set up NFS for this. Instead, I thought I’d try an Eclipse solution, the Remote System Explorer, and hook up everything using SSH.

First, I had to redirect a port on my laptop towards the qemu SSH port 22. The qemu option ‘-redir tcp:2222::22’ did nicely there and I was able to use it to log into my qemu using PUTTY on my laptop. I also decided to forward another port, 2345 to the same port on qemu to allow gdb on my dev machine to talk to a gdbserver on the target using that port.

I then set up the SSH connection in RSE on the dev machine. I used the ‘router’ address so that the dev machine would connect to Windows on my laptop, which then forwarded the SSH connection to qemu. It was tricky to figure out how to set the port number to 2222 instead of 22, but I found it and it worked like a charm. I used the Terminal view to log into the qemu session from VirtualBox. Cool!

I then tried the C/C++ Remote Launch feature that uses the RSE connection to download and launch into the CDT debugger. When I first tried, the executable on the target didn’t have the execute permission set, but once I fixed that, the debugger launched fine. Very cool.

Apart from being fun and interesting, this OpenConsole thing is giving me some real experience on using Eclipse tools to do embedded development with Linux and exercise all that it offers. I am very pleased with it and I think we really need to get the word out how well it does, like a Webinar or something 🙂

BTW, Go Rays!


