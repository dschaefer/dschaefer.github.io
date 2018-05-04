---
layout: post
title: 'Re: Don''t try this at home'
date: '2007-06-29 23:04:00'
---


As I mentioned recently, I had trouble with CDT for Windows with performance on my slower machine at home. Well, I’ve been able to trace it to the Harmony VM. Not only that, during testing, I was able to hang the VM when I went to do a CDT index rebuild. So for CDT for Windows 0.9, I’ve dropped the Harmony VM for now. The promise is there, but it’s clearly still a pre-release and they have some work to do to get it fast enough and to fix some other bugs that we raised against them as well.

So after switching to the Sun JRE, things are much better, even on my Core Duo laptop. And I was able to run it successfully on my 666MHz beast of a machine, albeit, it was still pretty slow, but no worse than everything else that runs there…


