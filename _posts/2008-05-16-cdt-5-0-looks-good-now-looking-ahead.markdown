---
layout: post
title: CDT 5.0 looks good, now looking ahead
date: '2008-05-16 09:43:00'
---


The CDT gang has put together a list of new features that are coming out with CDT 5.0 in a few weeks. [Check it out here.](http://wiki.eclipse.org/CDT/User/NewIn50) There has been a lot of work further improving the indexer and we have a new refactoring framework with a few refactorings available. And there has been a little work on the build and debug side as well.

It was a good sign this release that we had no major architectural changes and got to focus on quality. There is a new scanner/preprocessor for the CDT’s parsers but, trust me, that was much needed and Markus S did such a great job that we hardly noticed the change. Compared to the new indexer framework in 3.1 and the new build framework in 4.0 things went much more smoothly this time.

As I start to work on Wascana 1.0 based on this great work, I still notice a couple of areas that we need to work on for next year’s 5.1. First of all is the tighter intergration of the Debug Services Framework (DSF) that is being built by the Device Debugging project. This is a pretty cool framework that is highly asynchronous and extendible. I am working on integrating MinGW’s gdb with it as an exemplary integration both to help me learn DSF and to show others how to use it.

But to make this integration seamless, we really need to do something about the Launch Configurations. Right now DSF provides it’s own set, meaning if you have CDT’s current debug framework and DSF installed at the same time you get two sets. That’s going to be terribly confusing. And, from what I hear, every vendor that integrates their own debuggers with the CDT add in their own sets. I’d like to see if we can get a common launch framework in place to help solve this, assuming there’s support from the community for that.

The other big issue we’ve got to address is the CDT build system. We’ve tried to support two modes of build, using external build systems, and using Visual Studio-like internal build. External is easy. But, unfortunately, my feeling is that we’ve made things too complicated on the “managed” build side. There has been some great work done up until now by the committers, but we need to make sure we’re meeting the needs of the community and either address them or provide the extensibility to allow them to do what they need but still provide a common user experience.

My real objective is to provide a common user experience for all CDT users whether they’re using a commercial product or the standard open one. That means unifying the workflows for everyone. Maybe then it’ll make financial sense for someone or a group of someones to write a CDT book to serve all of the CDT community.


