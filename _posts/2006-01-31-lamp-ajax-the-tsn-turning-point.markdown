---
layout: post
title: LAMP &amp; AJAX - The TSN Turning Point
date: '2006-01-31 10:07:00'
---


If you were at EclipseCon last year, you may have seen the demo I gave of IBM’s Rational Application Developer to build a Web app that monitored a C++ app. I used gsoap to present a web service that monitored some value. I thought this was pretty cool way to web enabling C/C++ apps and maybe bring these apps into the Internet mainstream.

Mind you, I kind of ignored the size impact that the gsoap libraries presented and the added complexity of having to figure out how to define my web service (WSDL is not for the meek and RAD helped me a ton). In the end, it was probably overkill when all I wanted to do provide access to some status data to apps on the web.

Recently I have become curious about all the hype behind AJAX and LAMP. While browsing through some tutorials on XMLHttpRequest, it struck me. Well, all this really is is a remote procedure call back to the server, the same thing I was trying to do with SOAP. The URL is simply the name of the function you want to call and the GET/POST parameters are the arguments. Could web enabling my C/C++ app be a simple as handling http requests and providing the properly formatted http responses? I’m on a mission to find out.

While I’m sure SOAP has it’s purpose in the big SOA scheme of things, I am always cautious about oversolving the problem. Time will tell how big an impact AJAX and LAMP will have on the industry, but I’ve always found that the most successful architectures are the ones that are the easiest to learn and supported by free tools. With the recent announcements of Eclipse projects that address AJAX and PHP development and all the web presence these technologies have, they’ve definitely caught my attention.

(BTW, TSN is one of Canada’s two main sports networks. Every game, no matter what the sport, they pick a moment that they think decided it for the winner, the TSN Turning Point).


