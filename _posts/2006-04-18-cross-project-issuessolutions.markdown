---
layout: post
title: Cross Project Issues/Solutions
date: '2006-04-18 11:10:00'
---


One of the things I love most about EclipseCon is that I get to see what the other projects are up to. It was really cool to see the progress that a lot of the projects that were just starting up last year have made since then. One thing I’ve noticed though is that a lot of them need to solve similar problems. I’ve been pretty happy to see how these projects are starting to work together to find common solutions.

One example is the Remote System Explorer that IBM has contributed to the DSDP Target Management project. It presents a view of remote systems and provides a framework for attaching services that connect to those systems in various ways. Once people have heard about it, everyone is now taking a look. My friends at HP are looking at it as a solution to remote development for their servers (I suppose that’s very similar to how IBM uses it internally) that they’d like to contribute to the CDT. Also, I see that the Parallel Tools Project is now looking at it for remote development for their big supercomputer iron.

The question that comes to mind, though, is that if this is something that can be used by many other projects aside from embedded, is it problematic that this functionality resides in the DSDP project? My answer is that, well, the RSE actually resides on dev.eclipse.org. It is being **managed** by the DSDP/TM project. These are essentially two different things. Anyone can get at the bits and add dependencies to them. What could be problematic is the delivery schedules of the bits and making sure things line up. This is one reason that Callisto is so important, although releasing all at the same time is having it’s own set of issues.

One thing I’m certain of, though. As Eclipse continues to grow, we are definitely going to run into the very same issues I’ve seen in my past with very large software projects. These issues can get out of hand without good architectural control over what we are building in order to make sure that we have good user and ISV experiences. That includes everything from reducing duplication to having common API and UI guidelines. I know a lot of people hate having to comply with guidelines, but I’ve seen what can happen when they don’t and it ain’t pretty.

I think the question [Mike is really asking](http://milinkovich.blogspot.com/2006/04/seeking-balance.html) is what role the Eclipse Foundation should have in all this. I’m not totally sure what the answer is, but I believe the best architects are the guys mucking around in the code. They usually have their finger on the pulse of the beast and in the best position to make the right call at the right time. But what these guys really need is someone to help facilitate architectural decisions, i.e. bring the group together and to do some concensus building.

I’ve been lucky enough to attend one of the Eclipse Architectural Council meetings last December (I’m not a member but Bjorn graciously invited me to attend). There were some great minds in the room and Bjorn was doing a good job facilitating the discussions. But I don’t remember seeing anything publicized from it, and we had a great discussion on using TPTP’s AGR for UI testing. And, I can’t remember if any architectural decisions were made.

I think the processes are pretty much in place. I’m just not sure whether we have all the right people involved. I wouldn’t mind seeing what would happen if we brought the top senior committers to the table and asked them what they thought about this or that. I’m sure they already have all the answers. But then, these guys are also really busy getting their features done for Callisto…


