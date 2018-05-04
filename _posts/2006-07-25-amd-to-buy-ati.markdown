---
layout: post
title: "&quot;AMD to buy ATI&quot;"
date: '2006-07-25 08:38:00'
---


Now, have you not seen that headline enough yet?

Any time there’s a bit of a shakedown in our industry I’m always intrigued. It’s not what the industry analysts have to say about it, and certainly not what you read in the press release from the parties involved. It’s the story behind the story that piques my interest.

So, I blast through all the reports and try to piece together what is really happening and what it means to our future. For the AMD/ATI thing, the Inquirer yet again puts forth a interesting [view on the insider story](http://www.theinquirer.net/default.aspx?article=33219). Whether what they say is true or not we may never know, but I have seen a lot of rumors posted there that eventually became fact, including the AMD/ATI deal.

I do think that they present a good argument for what is happening, and it seems to be driven by the end of the MHz race (thanks, I can cook a roast in my PC case now, enough already!) and the push for many-multi-core a la Sun’s [Niagara](http://www.theinquirer.net/default.aspx?article=19423) architecture. AMD also has some pretty cool ideas on how to integrate co-processors that do cool things into their cache-coherent architecture and I’m sure the ATI acquisition will help speed some of these along. And the Inq is pretty sure Intel is working on similar architectures.

So what does that mean for us tools developers? Well, these events really give me more confidence in my prediction that a programming model change is a-coming. Applications will more and more need to take advantage of a multi-threaded environment to get performance gains. We can no longer rely on ever increasing MHz to save us. For C and C++, it means building more multi-threading constructs into the language. Something the [Parallel Tools](http://www.eclipse.org/ptp/) (PTP) people are working on building tooling for APIs like [OpenMP](http://www.openmp.org/).

As I’m sure everyone who’s built a multi-threading application (such as Eclipse plug-ins) know, working in this environment is difficult and somewhat unpredictable. The door is wide open for a new set of analysis tools that we can use to scope out when things are going wrong. And I’m sure our experience with such tools in the embedded industry, where we have had to deal with unpredictability of environments for a very long time now, will become of value to everyone.

It’s an interesting time again in our industry and we’ll all need to keep our eyes on it and be ready to hold on tight as yet another paradigm begins to shift.


