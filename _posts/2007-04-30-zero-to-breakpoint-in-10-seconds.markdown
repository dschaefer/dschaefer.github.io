---
layout: post
title: Zero to breakpoint in 10 seconds
date: '2007-04-30 12:30:00'
---


We’re getting close to our first release candidate, RC0, of CDT 4. One of the key objectives for CDT 4 was to simplify the new user experience. Thanks to some new features in the CDT like new project templates and in the Platform like contextual launching, we can now get you from a blank workspace to your first breakpoint in 10 seconds (faster if you type faster :).

Here’s how:

1. File->New Project.
2. In the New Project Wizard, select C++ -> C++ project, click Next.
3. Select the Executable project type, clicking the + and selecting one of the Hello World templates and if more than one Toolchain is listed, pick one. Type in the Project name and click Next.
4. Fill in the form with information the template needs to generate your Hello World app, click Finish (or next to play with the build configurations, but the defaults are fine).
5. Click the Build button in the toolbar, wait for the build to finish.
6. Click the Debug button (one click debugging!) and accept the switch to the Debug perspective.

And you’re done. The debugger hits the default breakpoint on main and you are set to go.

Give that we’re not done yet with CDT 4, there is a caveat at the moment. The one click debugging only works with the MinGW integration. To set that up, simply run the MinGW compiler and gdb installers from [www.mingw.org](http://www.mingw.org/), or have MinGW installed in C:\MinGW. The CDT will automatically pick up the install location. We’ll get the other ones (Cygwin, Linux, etc) working as by the time CDT 4 ships at the end of June.


