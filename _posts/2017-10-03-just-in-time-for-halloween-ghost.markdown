---
layout: post
title: Just in time for Halloween, Ghost
date: '2017-10-03 13:00:40'
tags:
- eclipse
---

When I started my blog [almost 12 years ago](https://cdtdoug.ca/welcome-to-my-blog/), I chose Blogger. For the time it was really cool, being able to easily create content on-line and publish with a click of a button. It served me well.

A couple of years ago, I decided I needed to upgrade my skills and learn more about web development. With servers at Digital Ocean only $5 a month, I dove in. Everyone seemed to be throwing love at Wordpress so I chose that and started [cdtdoug.ca](https://cdtdoug.ca) importing all my posts from Blogger. PHP and MySQL can be pretty taxing on a $5/month server but I managed to find settings to make it work. 

As things tend to go, we started doing real web development at work and I ended up using a lot of those skills I gained working with my own server. I learned a lot about AWS and quickly fell in love with the power of it. I chose to grab a free year and I migrated cdtdoug over to an AWS machine. I love how developer friendly Digital Ocean is, but AWS is, well, AWS.

Well, the free year ran out and I was running on a $10/month server. And I really wanted to do other things with this server and Wordpress was taking a lot of juice. Googling around for alternatives, [I ran across Ghost](https://ghost.org). Ghost runs on node instead of PHP and when run with the SQLite option, it's very lightweight and fast. If I become super famous, it probably won't scale, but I don't think I need to worry about that.

So I set up a new server, a $5/month t2.nano and migrated my Wordpress blog to Ghost with Disqus for comments. [I used mainly this guide (click)](https://www.ghostforbeginners.com/migrating-your-wordpress-blog-to-ghost/) and the Ghost docs themselves. It went pretty smooth and I'm pretty happy with it so far. It force me to learn Markdown (what was so wrong with WSIWYG?). And it leaves a lot of room, even on this tiny server, to do some IoT things I've been meaning to try. It'll do for now, until I get the itch to change it yet again.