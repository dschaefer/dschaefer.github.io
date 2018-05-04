---
layout: post
title: A Thought on a Componentized Future of IDEs.
date: '2017-03-13 11:56:08'
tags:
- eclipse
---


If you haven’t heard of the Language Server Protocol and the language servers they inspire, take a Google around. There’s something very interesting happening here. <span style="font-size: 1rem;">The direction the LSP starts, and we’ve had discussions around a Debugger Server Protocol as well, opens the door to the componentization of IDEs.</span>

<span style="font-size: 1rem;"> And this is quite different than the plug-in model we have with Eclipse. Instead of creating a UI platform and having plug-ins add menu items, preference pages, editors, views, etc., build your IDE from the other direction. Take a collection of components that don’t have UI, that implement IMHO the hard things about IDEs, language parsers, build systems, debugger frameworks, and wrap them with your own custom purpose IDE “shell”.</span>

Eclipse suffers to a significant extent the “Tragedy of the Commons”. There is a large amount of inconsistency between plug-ins that do similar things but do it in different ways. Why is there a Perspective for every language? Because each language plug-in developer has different ideas on how the “Code” perspective should be laid out. And maybe, for their users, they’re right.

An alternative reality has language plug-in providers provide APIs that allow IDE builders to provide their own user experiences. Yes, that would be a lot more work and probably not practical. But as the doors open to a new generation of IDEs, language plug-in providers need to think about how they’d plug into many of them. It’s not clear which one will be the winner or even if there will be a winner.

It’s a brave new world. And we have a way to go before we figure it all out. But it’s a great time to think outside the box and see what sticks to the walls, or in my case, what I don’t erase from my whiteboard ;).


