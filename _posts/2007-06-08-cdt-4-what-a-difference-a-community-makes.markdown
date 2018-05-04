---
layout: post
title: CDT 4, What a difference a community makes
date: '2007-06-08 09:34:00'
---


If you’ve ever been to a CDT meeting, chances are you would have heard me state one of my mantras, “Don’t take a .0 version of an open source project and put it in a product”. Certainly, in the past with the CDT this has been very true. And it certainly hasn’t been the fault of the committers and contributors to the CDT who work on it with a passion and really want it to be the best C/C++ IDE it can be. A lot of it had to do with the lack of test pressure we’d get on these releases. And a lot had to do with the lack of feedback from the community until after the release. A lot of it had to do with a young community that was just starting to grow.

Over the last year, this has all changed. With the great bug reports we’ve been getting from the community and the volume of patches we’ve been getting from contributors, and the great work of our army of committers, I am happy to say that CDT 4.0.0, is the first .0 release of the CDT that I feel really good about. I’m sure everyone will be pleased with it from our open source community to the vendors that adopt it.

In the spirit of openness, I have to admit I have been very dissatisfied by our previous .0 releases. And I think I need to share what happened so that we can learn from it. Here are the “lowlights” of previous CDT .0 releases (BTW, the CDT 1.x.0 series actually went pretty well, so we’ll start with 2):

- CDT 2.0.0 – first introduction of our new parser-based indexer and search. This was a dramatic change to the way we did indexing and the start of our performance woes. In fact I rewrote the CDT scanner (tokenizer) in 2.0.1 since it was brutally slow. We also introduced a new build model that wasn’t really ready for prime time and really needed to be exercised with more tool chains.
- CDT 2.1.0 – This release was to meet one of the contributing vendor’s product needs and was done while the other vendors were focused on the next release. It was a bit difficult to watch the extent of work they were doing mainly on their own. This really showed the need to standardize our releases (thanks Callisto, Europa, etc!) and how the model we had been following can’t scale as the number of contributing, and consuming, vendors increase.
- CDT 3.0.0 – This was the big DOM release. Again, massive changes to the indexing and search framework done by one vendor. Even worse, that vendor later had to withdraw its resources on that massive bulk of code due to business reasons. This really showed us the need to have a diverse set of committers working on each component. Contributors will come and go, and you need to build a robust community to survive it.
- CDT 3.1.0 – Yet another new indexing framework. With the contributors to the original index gone, I took it upon myself to finally throw out our failing assumptions, 100% correctness as a requirement being the big one, and focus on a new strategy to address performance. At the end of the day, this new strategy is the right one and correctness was still pretty good. The problem was that I did it myself and bit off more than I can chew. It was an absolute necessity to get it done, though, but I did do a lot more work for 3.1.1 to make it product quality.

It’s been a while ride over the last 5 years on the CDT (BTW, it was 5 years yesterday, I need to blog about that too!). I think we’ve learn a lot from it, probably enough to write a book about it. Being in the open, I hope others can learn from it too. At the end of it all, I think the most important aspect of any software platform project, commercial or open source, is that of community. And the most important job of a project is to build that community. And that there is probably nothing harder to do than build a community. As our industry goes through this shift, we really need more examples of what to do and what not to do. Then, hopefully, we won’t have to always go through pain like this.


