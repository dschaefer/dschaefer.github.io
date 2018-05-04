---
layout: post
title: Sustaining Open Source Projects Through Turnover
date: '2006-07-18 11:16:00'
---


When you have an open source project such as the CDT that has been around for a while, you end up having to deal with turnover in the people that are working on that project. There are usually a couple of reasons I’ve seen as to why this happens. Either they have been revectored or promoted to work on something else, or they’ve left the company that was contributing the resource to a company that doesn’t want to invest their resources that way. (As an interesting side note, we have quite a few examples now of people who have switched companies but are still working on the CDT, including yours truely, but that’s a topic all on its own…).

In dealing with turnover, I find myself going through a paradigm shift from young project to mature project. In a young project, you are struggling to get people and organizations to contribute to your project. So you find yourself accepting contributions that may not perfectly fit the mould and architecture you are trying to set out, but getting those contributions mean getting people involved and showing the world that your project has momentum and is “the exciting place to be”.

But with turnover, without proper documentation, automated tests, and good architectural fit, you start finding that that code that helped get your project going now becomes extra baggage. You start struggling to add new features and you find you need to either replace or simply remove the functionality it provided. Without someone to keep the code alive, it quickly gathers “rust” which starts to spread to places where you are trying to do new work.

So the lesson of the day for me is too keep the long term vision, including a well laid out architecture, for the project front and center from day one. Try to influence new contributors to follow that vision and to manage the churn in that vision so that you can sustain the code as long as you can. This is all basic software engineering school stuff, but it applies to open source projects as much as it does to commercial. And I think I am now of the opinion that having a strong vision like this can serve as much of a draw for contributors as a wide open door does. Or maybe the growth in the CDT lately has given me a bit more confidence. Or maybe its my new rose colored glasses…


