---
layout: post
title: Going Serverless
author: Doug Schaefer
tags:
- eclipse
---
# Going Serverless

Well, after a couple of years running my cdtdoug.ca server on AWS and the couple of years before that on DigitalOcean, I finally got tired of managing my own server and have moved my blog over to Github Pages. I'm using the default Minima template to get me going, but reading through the Jekyll docs, it looks like I'll have some fun tweaking my own setup the way I want it.

For the first 8 years of my blogging life, I had hosted it on Google's Blogger. But being the foolhearty geek craving to learn new things, I got my own little server in the cloud and moved my blog there, first on Wordpress and then recently moved to the much lighter weight Ghost. I learned a lot and it was pretty fun but I think I got what I wanted out of it and it's time to move on to the next thing.

The other reason for getting a server was to do some home IoT projects. I had visions of setting up my own MQTT broker there and a simple node.js web site to provide the UI. But the world has changed. I am now looking at serverless offerings that should allow me to do all this without having to manage a server and at a fraction of the cost of even the t2.nano. One device, a few thousand messages a month, a simple REST API and a tiny static web site. It's almost free.

So that's my next adventure. First, I'm hoping I've set up the Planet Eclipse feed to pick up the generated RSS XML file properly. Then I'm off to play with some new toys.