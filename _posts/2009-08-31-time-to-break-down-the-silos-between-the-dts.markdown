---
layout: post
title: Time to break down the Silos between the *DT's?
date: '2009-08-31 11:06:00'
---


What started out as a personal need for writing and debugging JNI-based applications, both based on Eclipse and for Android, has turned into something bigger, a lot bigger. The hardest problem we face for what I’m doing is supporting multiple debugger technologies in the same debug session and ensuring a nice seamless experience. Showing both Java and C/C++ stacks merged together and stepping back and forth between them would be the cat’s meow.

As I’m starting to hear from the greater Eclipse community, there is need for cross language/cross technology debugging in other areas as well. One example is Rhino which is being used by the e4 team to support writing plugins in JavaScript. Having a debug session with JavaScript and Java in the same stack would also be awesome. Similarly, we have JavaScript or ActionScript running in the browser interacting with a Equinox server, or maybe PHP running in Apache. Web applications are the manifestation of distributed applications and, as promised, those applications tend to involve multiple languages.

Traditionally, the language tooling projects at Eclipse have lived in silos. The CDT team has have very little interaction with the JDT team, for example. And that’s not generally the fault of the team members. It’s just a symptom of the lack of investment in Eclipse towards common technologies. Being an engineer, I have no idea how to solve that except to ineffectively whine about it. 😉

But one objective we’ve had with the CDT was to ensure that the C wasn’t just for C/C++. Many of our frameworks are language independent as much as we practically could. We haven’t had enough investment to be able to push that out to the general Eclipse community, but we do have projects like Photran (Fortran) and the fledgling Hibachi (Ada) and the new but remote ObjectivEclipse (Objective-C) doing that.

I think in particular, our new debug framework, DSF, could be used for much more than C and related languages. DSF started out as a solution for the difficult debug environments we face in the embedded space and actually started as the Device Debug project of DSDP. We’ve migrated it down into the CDT in 6.0. We’ve often quipped that it really should be down in the Eclipse platform itself. There will be challenges, technically and otherwise, to make that happen.

What I want to do is start prototyping multi-language, multi-debugger debug sessions based on DSF. That would initially include Java and C/C++. I’ll also take a peak at JavaScript debugging and consider how that impacts it. I’m confident the flexibility we brought with DSF can be leveraged to make the Eclipse side of this relatively straightforward. The bigger challenge will be co-ordinating the different debuggers.

If others are interested in this work, we should co-ordinate our efforts. Let me know and we could set up a mailing list to talk about this area, and hopefully we can start breaking down the silos.


