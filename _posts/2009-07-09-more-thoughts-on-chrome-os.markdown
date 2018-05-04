---
layout: post
title: More Thoughts on Chrome OS
date: '2009-07-09 19:45:00'
---


As quickly as it came, the hype has died down over Google’s announced Chrome OS. There hasn’t been much to stoke the fire so it’s died down naturally. And that’s a good thing. There’s a lot of lead time to figure out how we all fit into this story, if we want to fit in at all. Here are a couple of more thoughts that came to me as I read all the stories. BTW, it seems some writers have already played with the OS, or they’re making a lot of assumptions…

**Equinox as a local app server**

One of the coolest features of OSGi and the Equinox/Jetty implementation at Eclipse is as an app server. This is something I’ve always wanted to spend more time with. I don’t think Chrome OS will be successful without some means of running local applications and the marriage between Equinox and the Chrome browser is a natural. I’d hope the two of these groups are talking.

**GWT or SWT browser edition?**

To be honest, I’m a neophite when it comes to what’s happing with running Eclipse in browser mode, be it RAP or the new e4 SWT browser stuff. All I’ve seen are demos that try to make the browser look like a desktop app. I think that’s doomed to failure. The more you make it look like a desktop app, the more users are going to expect it to work the same as a desktop app, and that just isn’t going to happen.

I’d take this opportunity to reinvent my application’s UI, to break away from the paradigms that the desktop has locked us into and to come up with cleaner, more workflow driven UIs. Having good tooling is still a must. The Google Wave guys were quick to pour praise on GWT which they used to build the Wave app. I’d pick that if I were starting down this road.

**Is there a role for native in Chrome OS?**

Believe or not, I think the answer is yes. We’ll I’m sure you believe that I think that but anyway. Chrome supports the NPAPI native plug-in API that was started by Netscape/Mozilla/Firefox and is now supported by WebKit/Chrome/Safari and Opera. If you have the need for a high performance app that does it’s own rendering, like a game say, then NPAPI is for you. Google already does this for it’s O3D graphic rendering API. You can too.

Now, what you can also do with NPAPI is present your C++ objects for JavaScript scripting in the browser using this interface. Now didn’t Dave Thomas say something about C++ and JavaScript being the future in his Eclipse Summit Europe keynote last year?

**ARM versus Intel**

It’s not a secret that Intel has an offer to purchase my employer, Wind River, on the table. That hasn’t closed yet. But I have to agree with the analysts who see this will help ARM and it’s partners. More interesting, though, is that this will really be the first time that ARM platforms and Intel platforms will be running the exact same software platform. It’ll be pretty easy to see who’s netbook/smartbook/mobile solutions are better. More importantly, it’ll drive both of them to raise the bar, which at the end of the day benefits the consumer like good healthy competition does.


