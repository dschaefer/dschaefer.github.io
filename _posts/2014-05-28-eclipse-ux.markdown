---
layout: post
title: Eclipse IDE UX
date: '2014-05-28 10:49:39'
---


I’ll document here the things I’m working on for Eclipse UX. We learned a lot from our recent BlackBerry Momentics IDE releases and will be working to contribute those upstream so others can benefit and help.


## Launch Bar

The LaunchBar is a tool control for the toolbar that manages launch configurations and building and launching. (TODO: screenshot)

It’s also provides a framework which providers can offer automatically created configs so the user never has to create them themselves. You can use that, for example, to create launch configurations for C++ application projects.


## ToolBar Filtering

With Momentics, we filtered the toolbar so that only the LaunchBar, few select editor buttons, and the perspective switcher were shown on the toolbar. We wanted to control the user experience and grab that control away from the plug-ins and put it at the product level.

We did this by overriding the TrimBarLayout in our e4 model which then hid unwanted toolbars at layout time. We need to generalize this and provide a proper extension mechanism.


## Product CSS Overrides

As a product owner, I’d like to override various settings in the CSS independent of Theme. The immediate use case is the MRU editor setting. I want to be able do that for all themes shown in my product.

There may already be a mechanism to do that. If not, I’ll add one. It might also be interesting to allow the user to specify their own CSS settings as well to override the Product settings.


## New Project Wizard

The Eclipse new Project wizard is very old and out dated and doesn’t give visual clues as to the type of projects available. Other IDEs do a much better job of that.

We have a pretty decent new project wizard for BlackBerry that we want to restructure to make it more general and contribute to Eclipse. (TODO: screenshot)


## Dark Theme

Lars Vogel has done great work bringing a dark theme to Eclipse. I helped by get the CDT support in for Luna. I think it’ll be especially interesting for users who are coming from the command line world where text editors often have dark backgrounds and light text.

But there is still a lot of work to get done.

First, there are still a lot of editors that don’t have support for the theme. It’s hard to see black or dark blue text on a dark background. It’s too bad that we didn’t have a standard mechanism to allow plug-ins to adopt the colors they need so that changes to the themes are automatically adopted.

Second, the text editor colors we are using have usability problems. With a dark theme, bright colors grab your attention. We have some colors there that are pretty bright which inadvertently grab too much of the user’s attention. (TODO: Give examples).


## Multi-Language Framework

I’ve often heard the sentiment that it’s too hard to add language support to Eclipse. As an early developer of such support for C and C++ to Eclipse, I can concur. Xtext has brought us a long way, but it’s really only powerful enough to do fairly simple languages.

I’ve been looking at ANTLR 4 recently and playing with their sample ECMAscript grammar. It would be awesome if we had a framework that would take an ANTLR 4 parser and lexer and provide basic editor functionality. It could also provide API that let you build parse tree visitors that easily create models for the semantic highlighting, the Outline View, an index, etc. It needs special modes to handle lexing for syntax highlighting (which Xtext does with their internal ANTLR 3 implementation), and for content assist. It would be pretty awesome.

I have somewhat immediate needs for this. I want to add support for Qt’s QML which is based on JavaScript. We have an ANTLR 3 grammar for it that I can get idea from. But I’d like to build a reusable JavaScript parser that I can use there and maybe we can use to improve JSDT. I’ve started work with the ANTLR 4 idea and will create a separate page to record progress.

Once this is in place, I have two longstanding wish list items that this could help with. First is support for Objective-C to support Mac OS X and iOS projects. Second is C# to better support the Microsoft world.

Why would I care about those? Because Eclipse is uniquely positioned to support all programming environments. It’s an independent body with no strict platform affiliation so everything goes. We just need a good powerful multi-language framework to make it easy to add support for these platforms.


