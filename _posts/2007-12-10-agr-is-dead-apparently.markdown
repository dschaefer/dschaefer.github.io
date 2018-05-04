---
layout: post
title: AGR is dead, apparently
date: '2007-12-10 13:16:00'
---


One issue we’ve always struggled with on the CDT is how to do GUI testing of the CDT’s UI components. A number of us looked at different open-source solutions that would allow anyone contributing to the CDT to also contribute GUI tests. Some community members do use commercial tools for their internal testing. But we’d prefer something generally available for everyone.

Two solutions seemed to come out tops, albeit a very low tops. AGR from TPTP and the SWT port of Abbot. However each of these had two severe problems that prevented us from using them.

First, the Abbot/SWT port has been progressing very slowly to the point where we’re not sure it’s even alive. We do have one committer, though, that is looking at supplying them with patches and maybe that’ll bring it back to life.

AGR also had one big stumbling block, it’s dependence on the TPTP test framework. The CDT releng test run is a simple JUnit setup and we wanted to run our GUI tests as part of that without having to spend the effort of integrating the framework. [Bug 138369](https://bugs.eclipse.org/bugs/show_bug.cgi?id=138369) was raised to see if someone in the community could make AGR work in such a simple environment.

Well, today, we were notified that AGR has gone into an As-Is state (i.e. dead) and the bug was marked won’t fix. I personally recommend against marking bugs in the CDT as won’t fix, because, who’s to say someone won’t come along and try and fix it. Why shut the door like that. At any rate, it does point out that the community hasn’t really rallied behind AGR as a GUI testing solution.

So what is the current state of open source GUI testing frameworks for Eclipse? Is there something else out there? Or is there still hope for either of these technologies? Is there an EclipseCon talk on this subject?


