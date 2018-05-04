---
layout: post
title: JUnits are my friend
date: '2006-07-13 15:45:00'
---


Now I’m sure everyone who writes code in Eclipse is well aware of the power of the JUnit, but I just felt like expressing my appreciation for them right now.

I am in the middle of adding a few constructs to CDT’s new index that didn’t make it into 3.1.0 and was worried about whether the code I had just written was correct or not. Of course, the CDT is chalk full of JUnit tests for the DOM and other features, but in the mad rush to get the new indexing framework in I cut corners and didn’t write any JUnits for it. Instead, I had my new Index View that I used to browse the index and visually verify things. (Now that view was supposed to be hidden since it’s not quite complete but thanks to those who found it and have raised bugs against it :).

Well, now that I have a bit more time, I figured I had better make the plunge and start writing some. To my surprise, with the new indexer architecture it was actually pretty easy to programatically create a project, import some files from my test plugin into the project and run the indexer over them. I was then able to easily write some code to search the index and make sure everything was there that was supposed to be there.

Alas, of course, it showed me that it didn’t and I have to now go and find out why that reference to my enum didn’t get added. In the end, writing JUnits will have saved me more time than it took to write them. No more excuses. And thanks to Mr. Joe Unit for saving the day yet again!


