---
layout: post
title: ANTLR v3, Everyone's Parser Generator
date: '2006-05-07 22:27:00'
---


And now for something, completely different…

I’ve been toying with the idea of expanding my desires to better support Windows development to better supporting .Net development. There’s lot of interesting things happening there not just on the Windows side, but with Linux as well with [Mono](http://www.mono-project.com/Main_Page). Not to mention, there is a Java VM implementation that runs on the Command Language Runtime (CLR) called [IKVM](http://www.ikvm.net/). The IKVM is interesting because I just tried running Eclipse 3.2RC3 on it and, aside from a few ClassNotFound and IllegalArgument exceptions, things ran fine albeit a little slow at times. That raises the specter of writing Eclipse plug-ins in C#, but more on that some other time.

So, of course, looking for a break from the mad dash to finishing CDT 3.1, I started writing a parser for C#. I’ve been dying to try out the new version of [ANTLR v3](http://www.antlr.org/v3/index.html), which is in early access mode of the famous [open source parser generator](http://www.antlr.org/) written by Terence Parr. The biggest plus is that it promises to support LL(*) grammars, i.e. almost any grammar that isn’t left recursive or ambiguous. I’ve spent plenty of time trying to get ANTLR to accept modern complicated grammars such as C++ and Ada, but gave up after a little while because of all the effort needed to refactoring the grammar to meet LL(K) restrictions. (For the curious, LL pretty much means top-down parser which is generally how you’d hand write one, like we did with the CDT’s C/C++ parsers, and the thing in the parens is the amount of lookahead used to make decisions on which path to take. ANTLR v3 supports infinite lookahead, previously thought of as too expensive but Terence is proving us all wrong).

Well, I’ve just started and my initial report is “Wow!”. Every time I enter a rule that used to give previous versions of ANTLR as well as LALR parser generators such as yacc and bison fits, I get no errors. And looking at the code that gets generated, it looks decently efficient, using a special algorithm to make the lookahead efficient. Hell, at this rate, all I have to do is type the grammar as it’s given in the C# language spec and I’m done. Well, not really because the grammar as it is found there has left recursion and has ambiguities, but all these can be fixed with fairly simple refactoring.

I can’t wait for Terence’s beta in the summer, when hopefully he’ll have some documentation so I don’t have to guess at the syntax based on the examples. Also, he is changing the licensing of ANTLR and has rewritten the code so that he owns the copyright, which all means that ANTLR should be acceptable for inclusion with Eclipse projects (hopefully, cross my fingers). All of which should mean that it’ll be easier to write parsers for new languages that we want to support with the CDT’s code model, DOM, and indexing framework. Kudo’s to Terence! Now back to CDT 3.1…


