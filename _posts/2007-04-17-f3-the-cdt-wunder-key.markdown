---
layout: post
title: F3, the CDT Wunder-Key
date: '2007-04-17 13:22:00'
---


Unfortunately, I do most of my programming in Java (sorry Java-lovers, but I hate Java). But the JDT really makes it a breeze to write code for the CDT plug-ins. My favorite feature is F3, or Open Declaration. Whenever I’m investigating code, I like to go visit the implementation of some unknown method to see what it does. F3 lets me jump from class to class and get a quick overview of the system I’m trying to program against.

Well, I’m trying to do the same thing with the CDT. Before CDT 4, Open Declaration tended to be slow since it did a complete parse of the file you’re viewing and all the files that it includes. With CDT 4, we’re now only parsing the file and using the CDT index to get all the other declarations needed for that file.

As well, F3 tended to be hit and miss on whether it actually found anything. A lot of that had to do with the indexer’s need for build information that is often hard to provide. Also a lot had to do with information that we hadn’t collected yet, C++ template information for example.

With CDT 4, F3 promises to be a whole lot better. I’ll be spending a bunch of my time as we start to wrap up CDT 4 development on making sure it finds as many definitions as it can so that it can be as useful to CDT users as it is for JDT users. The one I just added that made me think of blogging about it is #include statements. Wonder what’s in that include file you #include’ing? Well move the cursor to the statement and hit F3. Bingo, there’s the include file (at least as long as the index knows where it is). I look forward to adding more cool features like that.


