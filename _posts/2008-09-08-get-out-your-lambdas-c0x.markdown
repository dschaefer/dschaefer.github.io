---
layout: post
title: Get out your lambdas - C++0x
date: '2008-09-08 20:47:00'
---


I saw a video of a talk by Bjorn Stroustrup, Mr. C++, who people I work with know I call “Barney”, affectionately, of course. In the video, he mentioned how badly he wanted to keep the name of the next major version of the C++ standard as C++0x and not have it slip into the next decade. Well, 2008 is almost over so it’s going to have to be C++09 if it’s to make it. But they are trying hard and making some progress.

And hopefully it does. C++ is due for a good shot in the arm, something to get people excited about. Working every day in Java as I do, and yearning for my C++ days, there are a few features in Java that would be exciting to have in C++. Not many, but there are a few :).

And one of them appears to be ready to be included in the standard, lambda expressions. Now Java doesn’t have pure lambda expressions, but the inner class support comes close. And with C++0x support for more general lambda expressions, I think we have a winner on our hands. Here’s an example:

  
int x;  
calculateWithCallback([&x](int y) { x = y; });

This ain’t your father’s C++. To explain what’s happening, we’re passing an anonymous function that takes a parameter y, and we pass along with it a *closure* which passes on some of the context with the function, in this case a reference to x. Later on the calculateWithCallback function does something and then calls our function with a parameter value for y. We then execute and assign the value to our x and return.

Anyway, very cool. Callbacks is a very popular design pattern and we use it all the time when programming Eclipse plug-ins. Being able to do something like this in a concise manner in C++ will be very useful and help bring C++ into a new decade, or whenever they get the standard ratified.


