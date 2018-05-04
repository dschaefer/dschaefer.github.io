---
layout: post
title: OSGi for native development?
date: '2008-06-13 09:31:00'
---


I hinted at this topic in [my last entry](http://cdtdoug.blogspot.com/2008/06/are-you-situationally-aware.html) and when giving [my crazy thought of the day last week](http://cdtdoug.blogspot.com/2008/06/crazy-thought-of-day.html). It’s another Friday, but judging from the comments to those blogs and my gut, I’m convinced now that an OSGi implementation for native development isn’t really that crazy.

Everyone has heard of the [Microsoft Component Object Model (COM)](http://en.wikipedia.org/wiki/Component_Object_Model). Even if you don’t chances are you’ve used it. It’s now getting long in the tooth but it was a critical technology that led to the success of the Windows platform starting with Windows 95. It was a great way to build up frameworks with plug-ins and to write components that used the services of other components, e.g. a Visual Basic script that ran inside Excel.

But of course, COM is very specific to the Windows platform mainly because of it’s reliance on the Windows registry which provided the directory to find the COM classes and objects you need. It also had some weird tricks with threading models and some wacky things called thunks to help to help performance when we were running Windows 95 on our old i486 machines.

But it’s been done and there’s lots of things we can learn from that, and from the limitations of some of the others, [like CORBA](http://en.wikipedia.org/wiki/Corba). Using C++ as the core technology is one thing we would need to avoid. Different compilers have different ABIs, like how virtual function tables are laid out. As much as we try to evolve, at the end of the day, C is still the best language for interoperability and almost every language provides a way to call C functions.

There was some discussion in the OSGi community around something called [Universal OSGi lead by Peter Kriens](http://www.osgi.org/blog/2007/10/universal-osgi.html) who is also involved in Eclipse. If anyone knows the status of that I’d be happy to take a look. It shouldn’t be too difficult to start with the OSGi APIs that make sense and start implementing a framework to support it.


