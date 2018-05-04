---
layout: post
title: OK, Eclipse, you have 3 seconds...
date: '2010-02-10 19:21:00'
---


Interesting enough, I had a couple of different conversations over the last couple of days on the topic of “What do we still need from Eclipse for it to be successful”. The context of success is the areas I work in of course, the CDT user space and Linux and Embedded in particular. Here, as I’ve blogged many times before, we still face an up hill battle to get developers to use Eclipse for their IDE.

From what I can see, it seems to come down to performance and start up performance in particular. Our users can easily and very quickly bring up vi to edit their code, run make to do a build, and fire up gdb to debug. That’s the workflow they are used to and their first reaction to being introduced to Eclipse CDT, which does a great job of wrapping this workflow, is “man that took a long time to start up.”

Start up performance isn’t all of the story. Many of the workflows in Eclipse are pretty foreign to them as well, but right now I’m focusing on the performance issue and whether there is anything we can do about it. I know there have been task forces over the years that tried to address it. I remember getting bugged about the CDT running at start-up. So if you have any information about the progress of those I’d be interested.

I guess to make the problem even more serious, we are getting compared with other IDEs, like Qt Creator and Visual Studio, which take maybe half the time or less to start up than Eclipse does. And it’s hard to justify to potential customers and users why that’s OK. It’s something that’s starting to get critical and we need to find an answer.

So, the challenge is, can we get Eclipse to start up in 3 seconds, about the most users will notice, a guideline I’ve used for other UI operations over the years. And it’s not just an objective. It’s time to start treating it as a hard requirement. People wonder why I’m a little negative on e4, this would be one of the reasons. My users need start-up performance addressed. And that will require a pretty radical change in thinking that will be at odds with many in the community.

But we need to start having the conversation. I’m looking forward to reading your comments. Please let us know what you think pro or con, or even potential solutions. The one I got from twitter that I like the most is rewriting Eclipse in C++. But I’ve said that before. Anything more practical?


