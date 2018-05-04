---
layout: post
title: Web apps make me think MVC
date: '2009-08-09 22:13:00'
---


I’m blogging more than I’m coding lately, so I’ll try to keep this brief. But I noticed someone mention MVC while I was googling around for practical information on GWT. After I thought about it a while, building a web app is a great example of the Model-View-Controller paradigm.

The model is data you store or derive on the server. You can use GWT’s RPC mechanism to get at this data. The Controller is also on the server. You can send commands, like build my project, to it via GWT RPC too. The server may then farm that out to other specialized servers to actually perform the action. The View is the JavaScript code running in your browser that takes the data and draws it using GWT’s widgets and invokes the control using GWT’s Handler mechanisms. Having a well defined RPC mechanism, and having a requirement to reduce the traffic over the wire to help with responsiveness, you get pushed to keep your web app MVC clean.

Now, relating this back to my mobile app interests, I can easily see the View portion of the app being replaced by the native widget framework for the particular platform. As I’ve mentioned in previous posts, I don’t think running a web app in a browser in a smartphone is a good idea. I know the browser on my Android phone is really slow. You’re better off using Android’s native widget set in Java to accommodate the form factor. That’s what mobile app building is all about. What I need now is an implementation of GWT’s RPC mechanism in Java using Android’s communication APIs, and really interesting things jump into mind.

What this leads you to is having three View implementations for my web-based IDE, that I’m now calling W-IDE. One in the web browser using full GWT, one in Android using Android’s native widgets but still communicating with the services defined in GWT, and one using the regular Eclipse desktop UI, theoretically using those services as well.

Now, yes, that’s three implementations of the same thing, and I know how that rubs people the wrong way. But my theory is that they are, in fact, not the same thing. Depending on which of the three you have, you are likely to need different workflows. Running Eclipse in a 24″ monitor, it’s OK to have all those views and taskbars and such visible all at once. In a browser running in a 10″ netbook, not so much, and you’d really like to make it page based to take advantage of the browser’s history mechanism. And in a 4″ smartphone, I really struggle with any workflows that make sense, but they certainly would be limited to one view or editor at a time.

At any rate, this is sure turning into an interesting journey of exploration. In the end, we may decide that this is all crap and IDEs are meant to run on desktops only and that using RAP’s server-centric architecture is OK to render in the browser (which if you can’t tell yet, I’m not sure I agree with). But this is a 5 year journey and we have time for the different technologies involved to mature and we’ll see. I think we have a lot of time to figure this out.

And, yeah, I guess I failed at keeping this short.


