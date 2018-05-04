---
layout: post
title: Java is making me dumb
date: '2009-05-28 22:21:00'
---


Sorry everyone who loves Java. But if you’re a regular reader, you know about my love/hate relationship with Java. I hate it because I can’t do the things I can do in C++ with it. But I love it because I’m making a pretty good living using it on Eclipse-based projects. So I deal.

Now, in my playing with Android and doing JNI development with it and OpenGL ES, I found myself immersed again in C++ for the first time in a very long time and loving it. One of the things you do with graphic programming is matrix multiplication. So I thought it would be cool if I created a Matrix class and an operator overload for the multiplication operator. So I could write code like this:

<span>M4 myTransform = baseTransform * currTransform;  
<span>  
<span>with all of these things as 4×4 matrices. Much less typing, no? :). So I coded it up and for the life of me I couldn’t figure out why it wasn’t working. Well, after mucking with it and trying different combinations I remembered something Bjorn Stoustrup mentioned in the C++ “bible”. If you aren’t doing anything special in your constructors, don’t provide them. The compiler will take care of it for you and will do a better job of it than you could. So I removed them, and bingo, it worked!</span></span></span>

Man I felt dumb, and at bit of a loss as to how I forgot how to do intense C++ programming. Clearly doing Java almost full time like I do, I’m out of practice. Now, you could argue that that’s why people should stay away from C++, because it’s too complicated. And, sure, it’s not for the meek.

But I was trying to show the incredible benefits the gcc compiler gives you with performance over Java, especially in mobile where the JIT’s aren’t up to snuff (and Dalvik in particular doesn’t even have one) and gcc can optimize using extended hardware capabilities like SIMD instructions. So there is a method to my madness and you put up with the pain to reap the rewards. Anyway, more on that after the Ottawa demo camp. Don’t want to spoil the show :).


