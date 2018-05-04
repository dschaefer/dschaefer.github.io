---
layout: post
title: Multi-Core Programming, Paradigm Shift Required
date: '2009-12-02 22:55:00'
---


I just caught myself sending 4 tweets in a row on the same subject. That’s probably a sign I have a blog entry topic at my finger tips.

I was reading an article entitled [“Microsoft’s top developers prefer old-school coding methods”](http://www.computerworld.com/s/article/9141465/Microsoft_s_top_developers_prefer_old_school_coding_methods). Whoever picked that title clearly missed the point of the panel discussion he was covering, but it’s an awesome read.

The panel involved a handful of distinguished engineers from Microsoft and they were discussing the future of programming technologies. And hilarity ensued! It reminded me so much of the discussion we had about JavaScript at the end of the Ottawa Eclipse DemoCamp last week. There was much hilarity ensuing there as well.

At any rate, I totally agree with what these guys are saying. Everything we’re doing to innovate in programming around graphical programming languages and concurrent programming is crap. Here’s some of my favorite quotes from the article:

re graphical programming: “when you have 500 things, graphical programming is completely unusable. You zoom in and zoom out and you lose all context. I think it’s just smoking dope.” (a similar comment was made about using JavaScript to build complete apps at the Camp).

re managed code: “lets developers perform above their level of competence. It’s like antilock brakes”. (They were talking about CLR, but I’d include Java in that).

re abstractness: “programming is getting so abstract, developers will soon have to use Microsoft’s Natal to write programs through interpretive dance.” (That I don’t want to see).

But the one quote that really confirmed what I had been thinking about multi-core programming: “It will be a long time before parallel programming becomes mainstream. Because of the bias towards sequention programming, we’ll still be reinventing ourselves as parallel programmers 12 years from now.”

This was a classic Ward Cunningham “A-ha” moment for me. I had hoped graphical programming could be an answer to break the sequential rut we’re stuck in. But the usability of building complex programs graphically kills that. I think at the end of the day, we still need to look at hardware description languages such as Verilog and SystemC as holding the key. They are all about concurrency since the hardware they model is too.


