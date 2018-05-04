---
layout: post
title: UML Action Semantics, Naturally Parallel
date: '2007-05-30 06:36:00'
---


Earlier in my career, I had the honor of reviewing a part of the [UML](http://www.uml.org/) spec which involved a very surreal phone meeting with one of my heroes in this industry, [Jim Rumbaugh](http://en.wikipedia.org/wiki/James_Rumbaugh). The area was on the UML’s Action Semantics. At the time it was a separate spec but it is now intertwined in the Superstructure document as UML’s Action behavior.

The idea according to Jim was to provide a sort of assembly language that all software behavior could map to. But I thought it provided a more powerful concept, that of the Action itself. An Action is a unit of behavior that has inputs, does some processing, and produces outputs. The outputs of one action feeds into the inputs of other actions. The “Ah-ha” is that all actions that have their inputs satisfied theoretically run in parallel.

This concept isn’t new. Hardware designers have been thinking this way forever. I believe [Petri nets](http://en.wikipedia.org/wiki/Petri_net) present a similar idea in mathematical terms. But what struck me was this was a really powerful paradigm that can make it easier for programmers to write highly parallel programs. What was needed, though, was a good, 2-dimensional programming language that allowed programmers to create actions and hook up the inputs and outputs quickly and, of course, with minimal typing. But something like that really wasn’t an objective for UML.

It’s probably one of the reasons I’m keenly watching [Eclipse’s Modeling](http://www.eclipse.org/modeling/) project. Aside from a great framework for creating domain specific languages, it has the capabilities that would be needed to build this “Action” language. And with a good back end that produced code for today’s multi-core clusters, I really think this could be a good way to help programmers meet [Intel’s challenge](http://news.com.com/Intel+Software+needs+to+heed++Moores+Law/2100-1012_3-6186765.html?tag=item) that “Software has to double the amount of parallelism that it can support every two years” to catch up to the what the hardware guys are doing.


