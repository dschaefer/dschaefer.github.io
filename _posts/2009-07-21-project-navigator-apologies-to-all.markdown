---
layout: post
title: 'Project Navigator: Apologies to all'
date: '2009-07-21 20:13:00'
---


I have to apologize to the Platform team and Francis in particular for my earlier complaint about duplicate entries showing up in the Project Navigator. It turns out that the problem was actually all CDT, or more specifically, how I set up the CDT part of my combo JDT/CDT/Android project.

By putting my source and build output into their own subfolders in the the project and setting the C/C++ Paths settings to point to them and not the root Project folder, the CDT stopped trying to display the other folders in the project in the navigator, the JDT folders in particular. No more duplication!

My disappointment has turned into happiness. I can now work on my Java and C++ files using the same perspective. The only thing that still doesn’t make sense is the tool bar where the new Class button still depends on the perspective, but that’s minor.

I’ll have to come up with some way to automate the creation of what I call JNI projects that have the mix of Java and C/C++ so others don’t run into the same thing I did. Maybe an improved Convert wizard.

At any rate apologies all around and thanks!


