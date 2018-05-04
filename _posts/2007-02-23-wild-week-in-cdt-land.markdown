---
layout: post
title: Wild Week in CDT-land
date: '2007-02-23 16:07:00'
---


Wow, it’s Friday. I’m glad. This week, once M5 was out the door, Intel committed their long awaited rework of the CDT build model. The idea is to make much of the good things we’ve done with the Managed Build System build model available to all CDT builders, and also available to the rest of the CDT that could really use this information. The parsers really need to know what compilers and settings are being used to parse properly. I can also see a use by the debug system to default to the best debugger given the currently active build configuration/<span>toolchain</span>.

As well, we get an upgrade to the New Project Wizard. I think the old approach of forcing users to select a language, C or C++, and then a build system, standard versus managed, was pretty intimidating to new users. How are new users supposed to know what a builder is anyway? With the new New Project Wizard, the selection of builder is hidden at least. It’s starting to look more like my previous favorite <span>IDE</span>…

What made the week busy was that to do this, a lot of the underlying architecture of both build systems changed. Of course, with any major architectural change, a lot of things broke. Mikhail S from Intel is working hard on all the bugs that are getting raised, and I was able to figure out how to get my <span>MinGW</span> and Windows <span>SDK</span> build integrations working in the new way, so we’re getting there. All the other <span>committers</span> are also measuring the impact of the change.

I think the biggest challenge is to get vendors who depend on these systems to take a look at the changes as soon as they can. Mikhail has been talking about these changes for a long time and has been publishing patches for everyone to look at for over a month. And it was still a surprise to many how vast the changes were.

While we do want grow the functionality and the architecture of the CDT, it is important that we don’t make too much work for those who are integrating. All I can do is encourage them to get in early and get in their feedback to <span>cdt</span>–<span>dev</span> and bugs in <span>bugzilla</span> as early as possible. I’m sure there are surprises in store for them, and for us on how they are integrating with the CDT in weird yet <span>intriguing</span> ways…


