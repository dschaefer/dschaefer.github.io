---
layout: post
title: Windows SDK RC1
date: '2006-09-02 11:48:00'
---


I’ve stated a few times now that although the CDT is highly used in the embedded and Linux/Unix markets, I don’t think we’ve conquered the world until the CDT is seen as a valid alternative to Visual Studio for Windows development. Looking at the whole Eclipse ecosystem and all the components available for it, I just think it has a higher value proposition than Visual Studio. At the very least you get a cross platform development environment that you can theoretically build any application with, once all the pieces are there that is.

So I’ve been working a little on adapting the CDT for Windows development starting with support for Microsoft’s C++ compiler. Over the last couple of years they’ve been shipping it for free, first as a separate toolkit, and now as part of the .Net 2.0 SDK. But, in order to get it working, you had to download a few pieces, including the Platform SDK, and if you wanted to do debugging outside of Visual Studio, the Debugging Tools for Windows. I felt it was pretty complicated to set up, especially for newbies, and of course these pieces aren’t redistributable so we couldn’t shrink wrap it for you.

But someone pointed me at the new Windows SDK which is part of the [Vista program](http://msdn.microsoft.com/windowsvista/downloads/products/getthebeta/default.aspx) (which is why I was confused since I thought it was a Vista thing only, but it is not). This SDK has recently reached [Release Candidate 1](http://www.microsoft.com/downloads/details.aspx?FamilyId=117ECFD3-98AD-4D67-87D2-E95A8407FA86&displaylang=en). As described in this [MSDN TV program](http://msdn.microsoft.com/msdntv/episode.aspx?xml=episodes/en/20060824WindowsMJ/manifest.xml) (these programs are pretty useful and something we should consider for Eclipse), this new SDK is really a combination of all the pieces you need to build Windows applications, both managed (i.e. .Net) and unmanaged (i.e. native).

What I found interesting was their focus on providing command line tool support for “people who like to work that way”. Now, I don’t know anyone developing Windows applications that like to work that way. So I read into it that they are really talking about 3rd party IDEs such as the CDT. With the tools provided by this SDK, it should be a pretty simple matter of integrating them as a tool chain just as we do with the gnu tools. Download the SDK, download the CDT and the Windows integration, and you are off and running.

At least that’s my hope, which of course will only be successful if it receives community attention. But it sure would be a boost for Eclipse to be seen as the development environment for everyone, without prejudice.


