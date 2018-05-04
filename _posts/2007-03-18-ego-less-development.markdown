---
layout: post
title: Ego-less Development
date: '2007-03-18 15:06:00'
---


I remember early on in my CDT career running into an old boss and mentor. He asked how things were going and I told him great and that we were starting to build a C++ parser for the CDT. He was skeptical that we could do that and make it work well with the time and resources we had. But I was so excited to be building a C++ parser, I chose to put aside his wisdom. “It’s not that hard.”

Well, for years after, looking back now, I probably should have listened closer to him. The CDT’s parser performance was abysmal. I really feel for the guys at QNX and others who were building products based on those early CDT releases. And, of course, you can guess what my first task at QNX was when I got there. Fix it!

Luckily I pulled a rabbit out of my, uh, hat. CDT 3.1’s indexer is incredibly faster than our previous tries. I totally changed the approach we had taken and threw away the requirement of being 100% accurate that we had be preaching in futility since we started. Now, each file gets parsed only once and again only after it is saved. A lot of good work has gone into CDT 4.0 as well to add more information to the index so that we can use it for all parser based features making them incredibly faster too. It’s not 100% accurate, but for 99% of CDT users, that’s just fine.

But I still remember those years of pain as we fought hard to make the parser faster. Everything we tried resulted in only minor improvements. And every time we analyzed the issue, nothing really jumped out as to the cause. Unfortunately, it was probably our egos that kept us from giving up and trying a whole new approach. And if we had taken that approach earlier maybe we could have saved so many in the community the grief of an indexer stealing all their CPU on them.

“Ego-less development” is a mantra of mine and we should have followed it. Always question your design, try to understand the big picture and the impact of your design on the entire system. And if someone points out a flaw, listen and make sure you really are doing the right thing. I think this is especially true in open source with so many eyes on your work and so many hands trying to pull it in different directions. It’s a huge challenge but if you are successful, the rewards are great, for everyone.


