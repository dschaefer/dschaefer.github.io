---
layout: post
title: Web server on your phone?
date: '2006-06-04 10:26:00'
---


One of my “too many” interests in the computing industry is how to best serve up web content from embedded devices. The main use I see for such a capability is to allow maintenance personnel an convenient and standard way at getting at state and configuration information from the devices under their care. You see it very commonly used for configuring home routers such as my Linksys.

If you were at the CDT BOF at EclipseCon 2005, you would have seen a demo I gave of using gsoap to do this kind of thing. Since then, I’ve come to the conclusion that SOAP and related protocols are oversolving the problem. You can do what I was trying to do with simple http GETs. And with the coming out of AJAX to provide more interactive content with web pages using simple http requests, this really starts to look like the right architecture.

The problem I had was how to you integrate an http server with your embedded application. There are a few httpd library packages around but none of them appear to have enough momentum behind them to take the industry by storm. I had considered making my own but going through the http spec I quickly came to the conclusion that it would take a little more work than I wanted to soak into it at this point.

Then I ran across [Nokia’s Raccoon project](http://sourceforge.net/project/showfiles.php?group_id=167580) where they’ve ported Apache to the Symbian OS that they use in their cell phones. My head almost fell off. I thought Apache was this big monolithic web server that is driving the bulk of the web servers on the internet, big iron types. Could Apache be made small enough to fit into embedded devices. Nokia seems to have been able to do it. And looking at Apache’s modular architecture, it looks like you could write some cool modules that can interact with the software on the device without having to resort to the slow and clunky CGI interface. Very cool, and something I need to look into more.


