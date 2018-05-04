---
layout: post
title: Sun GPL's Their Java
date: '2006-11-13 11:32:00'
---


We’ve all been waiting to see what Sun will really do when it talks about open sourcing Java. I noticed there was a lot of mistrust amongst the open source communities, but I have no prejudices against Sun so I kept an open mind.

Today (well actually over the weekend some time), Sun officially turned on the pipes and you can download it. You can see it all at [java.net](http://www.java.net/). There you will find their implementations for J2ME and J2SE as well as J2EE which they had open sourced earlier. For J2SE, they only have the VM and compiler open sourced. I guess they are still working on 3rd party licensing issues to get the complete JDK contributed.

They have chosen GPL as the license with the classpath exception on the libraries so that you can link commercial code without being affected by the GPL license. I’m always a bit cautious about GPL and you really got to be careful when using it but I think it’s a pretty good choice that will help avoid the forking that Sun has worried about and enable the JDK to be shipped as part of Linux distributions, which has been a pain in the you know where in the past.

Time will tell, however, how well Sun can build the community around it. If they begin to allow committers from outside of Sun, I think you’ll see over time the mistrust fade. But if it becomes apparent that they aren’t that serious about letting others play in the sandbox they’ve made, then it will all be for naught. But if it is successful, it’ll be interesting to see how the Apache Harmony project is impacted since they are essentially duplicating effort but with a different license. We’ll need a magic decoder ring to figure this all out…

So being the hacker that I am, I drove directly into the source tree to see what the code looked like. They are using subversion, which I really hope that we at Eclipse.org will switch to one day. I also see that the VM code is written in C++ and looks pretty clean. Which, of course, brings up the question on whether you can use the CDT to work on it. Of course you can! And I’ll have to spend some time in the upcoming weeks putting a tutorial together to show how.

Interesting times ahead, of that there is no doubt.


