---
layout: post
title: You want to do what with EFS?
date: '2007-11-09 10:25:00'
---


In my last entry, I dropped a quick note about a feature I’m planning for CDT 5.0 due out with Ganymede next summer. We are getting more and more requests from users moving over from Microsoft’s Visual Studio that the CDT should do things like in Visual Studio. One of the high runners is to be able to add files and directories from anywhere in the file system to projects, and to be able to exclude files and directories from other directories. You could use Linked Resources to do the ‘add’ today. But there’s no mechanism to do the ‘exclude’.

After playing around with EFS for remote project support, I got the feeling that I could do this add/exclude functionality using EFS by implementing my own file system that would map paths requested from IResources into real file system paths the users wants them to map to. I’ve decided to call this the Flexible File System (or ffs for short and as the schema name).

I’m not sure if this is going to work out yet. The simple things like opening files and building the resource tree should work. I really want to get the Team system working as well so you can keep the files in source control. That will be the really tricky part. I also think there is going to be a lot of issues we uncover where we’re assuming we know the layout of the file system. And we got to figure out how to tell the external tools the real file locations they need.

For now, I’m only looking at this from a CDT project perspective. I know there are a lot of other projects that could use this and I hope we can move this to the platform at some point. And it won’t do some other things with the resource system we’ve always wanted, like nested projects. But now that we’ve reached a good level of maturity with the CDT, we need to start addressing these issues and remove those final big objections to moving to the CDT and Eclipse.


