---
layout: post
title: Ever rising expectations
date: '2007-10-25 11:44:00'
---


You know there was a time when I though syntax highlighting was a cool feature. It made it easier to see your code by allowing you to focus on the things that are important, like the names of functions you call and variables you have. With the correct coloring, keywords tend to slip into the background where they belong.

Well, content assist with STL iterators doesn’t work. If you define a Class A with a member x and you have a list[ of them, you want the iterator i-> to give you the x. No, really, it’s the cat’s meow of content assist – interpreting the i to find out it’s a iterator template instantiated on A then resolving A to find out what it’s members are. The unfortunate thing is that this used to work up until CDT 4 when we moved content assist to use the new index framework instead of always doing a complete parse. It’s much faster now, but we don’t have all the necessary information about templates in the index yet.]()

And, of course, with our active CDT community, people are starting to raise bugs on various things that aren’t working with templates. For C++ developers, the Standard Template Library is an awesome tool. It greatly simplifies the code you have to write to use generic collection classes and it does it with all the type-safety and performance that C++ is famous for. I guess I shouldn’t be surprised that people expect the CDT to work with them as well as it does regular C++ classes.

But, under the hood, this is an incredibly complex beast. When we got it working first in CDT 3.0, despite the somewhat slow performance, I was proud of the team that we were able to make something like this work. It was a lot of effort by some really smart people, who unfortunately have moved onto other projects. And luckily we have a new set of really smart people who will continue the effort as we move to the new index. So we will get it working again.

It is very interesting to see, though, the expectations that IDE users have now. It certainly has come a long way. Once we get the template thing done, our next biggest demand is C/C++ refactoring and we have some more smart people lined up to look at that. If you were to start a new C/C++ IDE today, it would be a daunting task to meet these expectations. I’m glad we have the history and the team we have now on the CDT so that we have a chance.


