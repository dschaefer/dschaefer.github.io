---
layout: post
title: Trust Matters
date: '2007-10-16 10:38:00'
---


I just finished reading [this article](http://www.spectrum.ieee.org/print/5598) on a recent failure with the International Space Station. Something caused all three Russian-built computers on the ISS to fail at once while the Space Shuttle was docked and the Americans were installing a solar panel. I love reading post-mortems like this and wish we did more of them in the software industry. You certainly learn a lot about what can go wrong on a project.

In this case, they found the problem to be with condensation causing corrosion of power lines and an eventual short. That caused an unfortunate chain events that activated an unfortunate feature, a single command that would turn off all three computers, nullifying the triple redundancy. Once that was identified it was easily and “creatively” corrected and everything is fine now.

But the thing I got most out of the article is that one of the bigger problems was the original incorrect assumptions made by the team that caused the determination of the real problem to take longer. Being from different countries, they team started out by blaming each other for the failure instead of taking a non-partisan approach and trying to solve the real problem.

This is something I try to do as much as I can, which is unfortunately not often enough some times. If there’s a problem, start with the assumption that I screwed something up. None of us are perfect and that group starts with me. That helps me take an honest look at the situation and if it is my fault, we can find it quicker. If not, then the fact that I’m not trying to hide from the problem should help there too.

When you are involved in an open source project with contributors from different companies, especially when the companies are competitors, you can end up in the same scenario. It is hard to build trust in those situations, and when your building something complex and run into problems, that trust becomes very important. To be successful, you need to trust that the other people are doing a great job. If you fall too quickly into the “blame game”, you’ll only get the project, and yourself into deeper trouble.


