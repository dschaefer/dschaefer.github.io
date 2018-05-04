---
layout: post
title: I'm not anti-e4, I'm just busy with other things
date: '2010-06-18 15:26:00'
---


As we start the discussion about CDT and e4 on the cdt-dev list, I just want to make sure people are clear when I make statements that appear anti-e4 that I’m not anti-e4. If you like e4 and you want to use it in your project, go for it. There’s some really cool things there and the guys are doing a great job of pulling it together.

But I have other important problems to solve higher up the stack than I see e4 trying to solve. In CDT-land, our biggest issue is getting people to even use Eclipse who are using emacs or vi and gdb just fine and who struggle adapting to the world of IDEs. We need to focus on enhancing the value of Eclipse and simplifying adoption to make it more appealing for these people to buy into our wares.

At the top of our list are some workflow issues and the flexible resources work that started in e4 but moved in to 3.x is a start on that. I think we still need some work on build to support multiple build configurations per project, and for build to work just as it does from the command-line. And the launch UI is over complicated for what our users need. But those things are all the platform stuff we really need. And we do have people trying to make contributions in those areas.

And, we have some things to work out in our own kitchen. We need to fix up the CDT build system so that vendors aren’t so frustrated by it that they end up writing their own. Then there’s the world of debug and systems analysis where I think we really need some innovative UI approaches. As starters, I don’t think you can visualize a massive multi-core system using a 2 dimensional UI that assumes a single context. I’d love to see something like Clutter in SWT.

So while the world is rushing towards HTML5 and the cloud, that’s great and everything, but we still have a lot of work to do to make Eclipse a great IDE on the engineer’s desktop.


