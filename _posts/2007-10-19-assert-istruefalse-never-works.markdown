---
layout: post
title: Assert.isTrue(false) never works
date: '2007-10-19 09:51:00'
---


In case you were wondering, this pretty much throws an exception every time. Although, I one of my first mentors often tried to blame stray electrons on some bugs so, I guess if he was right, there could be times when this does work. But I wouldn’t put money on it.

I ran across this particular piece of code when it showed up in a bug report recently. It came at the end of a if-then-else chain as the else that the author didn’t expect to ever run. Well, this one unfortunate user found some way to make it run. Maybe it was a stray electron, or maybe it was just a corrupt preference store. We’ll have to see.

But this did bring up another of my mantras for software development. Don’t throw an exception that you don’t plan on catching. Sometime we use exceptions as a crutch. If we get to some point where we can’t figure out how to continue, we just throw an exception and don’t need to worry about it any more. At least until the exception bubbles up to the UI and the poor user has to deal with it.

It’s a tough job to put in all the possible error handling for a given situation. If you’re building a safety critical system, you get a whole boat load of funding to pay for that effort. But when you’re building a software development tool, you often feel that you don’t have the time to work on code that you don’t think will ever run. But it really does pay off in the end. When you have hundreds of thousands of users of your software, there’s a pretty good chance one of them will run into a stray electron or two.


