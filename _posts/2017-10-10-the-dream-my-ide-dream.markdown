---
layout: post
title: The Dream, my IDE Dream
date: '2017-10-10 18:08:34'
tags:
- eclipse
---

Let me tell you a story.

I got into work today and found an e-mail in my inbox from my boss. A customer was having an issue and he wanted me to look at it. He included in the e-mail a link to the JIRA. I clicked on the link and it opened up.

The good news is that the JIRA included an analysis from our fault analysis AI engine. I clicked on a link and it brought up the report.

The engine had seen the same crash the customer reported a few times and analyzed my source to pinpoint where it was wondering if a value passed into the API was not being handled properly. OK, let me try this in the simulator with the debugger. I click a link and git checks out the corresponding version of the software stack used in one of the crashes.

Running it in the debugger, I see, that yes, the engine was right. One of the clients was passing in a value that I wasn't expecting. So I added code to handle it and ran it with the simulator again. Worked there, but to make sure I changed the target selector and to run it on some real hardware. A VNC session opens up and I can see that it fixed it there too.

I then click commit. All the relevant information from the investigation so far is automatically added to the commit comments and I add a quick line apologizing for missing this scenario and click submit to Gerrit. The review opens up and I do a quick check to make sure everything I wanted was there. I then see that the verify job has started up on Jenkins and I go for a coffee.

When I get back, I have a notification that the verify job has failed due to one of the tests failing. I click through to see the test and click another button for git to checkout the test and to start it running on the simulator under the debugger. A breakpoint is hit at the failure and I see I messed up the handling for the value it was passing in.

I make a quick fix, run the test again. It passes. I run the test I was doing for the original scenario and see it's working too. I amend the commit and resubmit. The Jenkins build passes and I do the final commit to the branch.

A few days later, I get a notification from our fault analysis AI engine. It has noticed that since my change, the crashes no longer happens. With that confidence, I mark the JIRA as verified and the customer is happy.

This is what I want from my IDE. I didn't use the term IDE in the description because everything I interfaced with to solve the customer's problem was the IDE (yes, even the mail client). We have all of this already, except maybe the AI engine, but that will come. What we're missing are the little things we get from these tools knowing about eachother. It's the "I" in IDE!

Mik Kersten envisioned this many years ago when he invented Mylyn. And I've seen a lot of this in IBM's Jazz. I think a lot of those ideas were ahead of their time and on a platform that struggles with being this complete environment. Workflows start with the cloud for the analysis phase, then meander into the desktop code and debug environments to test and fix the problem, and then back into the cloud for verification and closure.

The next generation IDE needs to seamlessly blend these tools so you don't even notice where things are running or even when you've switched between them. You know you're using a great IDE when you don't even realize you're using it.