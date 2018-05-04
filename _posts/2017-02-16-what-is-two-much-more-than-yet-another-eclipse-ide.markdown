---
layout: post
title: What is Two? Much more than yet another Eclipse IDE
date: '2017-02-16 14:19:58'
tags:
- eclipse
---


It’s been a wild few weeks on the journey I now simply call “Two”. (Until it becomes an Eclipse project, I can’t call it one. And rightly so). The feedback I’ve received, especially as it hit the presses, was fantastic. It’s driven a lot of traffic to [my github repo](https://github.com/dschaefer/eclipse-two.). I’ve even received a few pull requests from people cleaning up my mess as I plow through it. At the very least, people are intrigued by idea of an IDE built with Web UI technologies running locally under Electron.

As I work through the vision, I don’t think it’s fair to simply call it yet another Eclipse IDE. It’s much grander than that. For me, Two is about that vision. It’s more than a code editor. It’s more than just taking the existing Eclipse IDE and implement it in HTML5 running locally. It’s about a whole new way for developers to work with their tools and access the resources available to them on the web.

Developers today have access to many powerful web services. Github is a huge one. At Eclipse we use Bugzilla for bug tracking. A lot of companies use JIRA. People may be using Gitlab as their private Github. You may be using Gerrit for code reviews. I notice LLVM is using Phabricator for code reviews. And there’s the venerable Review Board still active today. Jenkins for continuous integration. And don’t tell me you don’t cut and paste error messages into Google searches to find others who’ve seen the same problem and worked out a solution. The Web is a critical tool in the developers belt.

I was intrigued by an [article written by the creators of a tool called Ship](https://www.realartists.com/blog/ship-20.html). It’s a Mac native, i.e. Cocoa, app that integrates with the Github issue tracker. This quote hit me:

“A point of pride for us is that many people we have shown Ship 2.0 haven’t been able to tell where the web-based content ends and the native Cocoa stuff begins.”

That’s exactly it. If we can say the same for Two, where you can’t tell where the web ends and integration with local tools begin, then we’ve hit a home run.

Integrated Development Environments provide the most value when they have integrations between tools, which the developer has had to do manually for years. The IDE’s role is to automate workflows that transgress all the tools the developer has to use, where the workflow becomes the key, not the individual tools themselves. This focus makes it much easier for them to accomplish their objectives, so they don’t have to learn all the intricacies of underlying environments, but provide a unified language.

And that’s what Two needs to be, a tools integrator that includes not only the tools the user has installed locally, but also integrates with these super powerful web resources in seamless workflows.

The other important factor with IDEs that so many forget, is that experienced developers will always have a bit of mistrust in their IDE no matter how good it is. They need to be able to get close to the iron and run the underlying tools manually at a place where their trust is higher. An IDE that hides that, or makes those tools hard to get to, will struggle being universal. That’s why I’m not a fan of Cloud or Docker hosted tools. In making deployment easy for the provider, they make it hard for the user to touch the bits they’re creating.

The main reason I don’t want to call this Eclipse Two is that this isn’t just about a next generation Eclipse IDE. That IDE was my One, the first IDE that I’ve had a hand in creating. I want to rethink the whole developer experience and create an IDE that works well in the modern world, now almost 20 years after One. [This is Two](https://github.com/dschaefer/eclipse-two).


