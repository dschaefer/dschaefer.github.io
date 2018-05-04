---
layout: post
title: Bye-bye 32-bit Windows
date: '2007-05-17 14:03:00'
---


[I just read](http://slashdot.org/articles/07/05/17/1452228.shtml) that Microsoft was putting an end to 32-bit support with their operating systems. I guess that shouldn’t really be a surprise. It is a real struggle for device driver writers to support both and I think Windows 64-bit has really been hurt by that. The same is probably true for Linux as we don’t see much demand for the 64-bit Linux version of the CDT either at 2.5% versus the 32-bit Linux at 20%.

Maybe this will finally trigger people to focus more on 64-bit and start writing programs with that in mind. The biggest change for C/C++ programmers is the size of pointers changes. I’ve seen a lot of code that assumes you can merrily cast a pointer into an int and back and everything is happy. One example of this is with Java native code where we like to stow away pointers in Java fields for later calls back into native-land. Well with 64-bit, while the size of pointers change, the size of int does not. I’m also hearing that there are different interpretations of the sizeof(long) where on some platforms it’s 64-bits, but on others it stays as 32. Then there’s long long (gcc) and int64 (msvc) which in the 32-bit world also means 64-bits.

Suffice it to say that the 64-bit world gets a little messy. We’ll think back to the simple days of 32-bit with a sigh. But then, I think things will still be better than the now ancient 16-bit world was (now who’s old enough to remember that?). Now they say that this will start after 2008, but given the length of time it took to get Vista out, people with 32-bit only machines shouldn’t worry too much. They’ll be ready for the dumpster by then anyway. And do we really need another operating system version beyond Vista? Microsoft hopes so, and I’m sure they’ll use the 64-bit push as a marketing ploy to help you think so too.


