---
layout: post
title: Eclipse p2, sweet!
date: '2008-03-28 10:08:00'
---


As we hinted at EclipseCon last week, my team has been [evaluating p2](http://wiki.eclipse.org/Equinox_p2_Getting_Started) as the framework for our new installer technology. We’re essentially coming from an InstallShield world where we have these big monolithic setup.exe type things and we are looking to make our installs more flexible and open the door to electronic distribution. It’s an exciting vision and we’re pumped to be working to make it happen.

I’ve talked to the p2 team off an on over the last while trying to get a sense of what they were doing. But it really took Pascal’s p2 long talk for it to really hit me. p2 is the new Update Manager (duh, that’s what they’ve been saying all along). But as I look under the hood, it’s an Update Manager on steroids (good thing there’s no drug testing of software). And it’s really got us excited.

The beauty of it is the extensibility. The underlying concepts are sound and based on some pretty standard notions albeit with weird names. InstallableUnits and Artifacts, what’s the difference? Once you get past that you’re fine. But the fact that you can override how things are installed with Touchpoints, and the fact that you can override how the Repositories are stored opens the door to some really exciting opportunities.

Aside from my internal work, I am looking to make a p2 based installer for [Wascana](http://wascana.sourceforge.net/). Yes, it can be used to install the Eclipse bits for the Platform, CDT and other plug-ins I need. But it should also be possible to use it to install the toolchain and libraries as well. What also struck me is that I should also be able to install the bits directly from their own download sites. This will allow me to quickly make available new releases of the components. The flexibility will still allow me to create off-line installs as well.

Another thing that popped into my head was whether p2 could be adapted to install Linux packages. Every distribution pretty much has it’s own package manager. It would be very interesting if we could get p2 to install RPMs for example allowing us to use the same UI to set up Eclipse as well as packages, or even allow us to set up dependencies between them. Then we could create a Linux toolchain integration plug-in that depends on the compilers and have the p2 installer install the whole thing.

So as you can see I have big dreams for p2, probably more than the p2 team can handle at the moment. But it’s an area that I really want to get involved in and contribute. And we’ll see where we end up.


