---
layout: post
title: Now where's that include file?
date: '2008-07-17 13:33:00'
---


Yeah, C++ refactoring is our biggest achievement for CDT 5.0. But here’s one I found probably more useful in my day to day use of the CDT (which is getting more and more lately which is awesome).

I have a burning need to learn GTK development. I have a little dialog based app that needs to run on Windows, Linux, and Solaris. I have the Windows version done using MinGW’s support for win32 programming (now there is an experience for you). Now I need to implement the same thing in GTK for Linux and Solaris.

So I’m going through the GTK 2.0 tutorial on the GTK web site and the first thing it get’s me to type in is:

  
#include <gtk>  
</gtk>

The first thing the CDT does is throw up a warning marker on the line complaining that the CDT indexer couldn’t find that include file. Being suspicious, I did a build and sure enough the header file wasn’t found. With all the great work the indexer team is doing I really should trust what it’s telling me.

So I fired up the Ubuntu package manager and found out that the GTK devel package is indeed installed. What’s up?

Then I remembered one of the new CDT features I stumbled across in my 5.0 testing that we really should tell people about more. I went back to the #include statement and after <gtk a="" about="" all="" alt-="" and="" assist="" being="" bindings="" but="" can="" cdt="" content="" ctrl-space="" dirs="" emacs="" enough="" examples="" files="" for="" gather="" great="" gtk-2.0.="" help="" i="" improve="" include="" including="" information="" it="" just="" key="" little="" me="" needed="" of="" offered="" one="" people="" pressed="" productivity.="" rest="" sure="" tell="" that="" the="" thing="" time="" to="" use="" with="" you="" your=""></gtk>


