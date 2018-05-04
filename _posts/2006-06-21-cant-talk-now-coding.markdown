---
layout: post
title: Can't talk now, coding...
date: '2006-06-21 09:45:00'
---


I’ve been pretty quiet lately with the blogging. The main reason is that I’ve been working certain parts of my body off as I try to implement a new indexing architecture for the CDT. There is a lot of good news and a little bad news with this project. The good news is that I can now index Mozilla in 14 minutes on my laptop! In CDT 3.0, that took around 50 minutes, and improvement of around 75%. As well, as you change files, you hardly notice the indexer running were as it could take up to 12 seconds to deal with the change in 3.0. I almost fell over when I got the first timing at 14. Followed shortly by a dance of joy.

How did I do it? Well I took a hint from the precompiled header feature that most compilers are starting to support. As I’m indexing, and potentially other parse activities as well, I skip over header files that I have already parsed previously and get the symbol information from the index. This required building a more structured database for the index as opposed to the string based flat table in 3.0. It turns out to be much faster since parsing C and especially C++ is a lot slower than the database lookup. This is why incremental times are so fast. I just didn’t realize the whole reindex operation would be so fast as well (my target was 20 minutes for Mozilla).

The bad news, is that while it is incredibly faster, it does suffer from being young. There is less captured in the index than there was in 3.0, for Mozilla about 20% less symbols. So searching for certain things aren’t going to get you everything you were looking for. But I have been able to capture the high runners. More bad news, is that we are getting spurious StackOverflow errors because not all information is in the index and some of the algorithms we have for symbol resolution weren’t prepared for that. So as a result, the new index is only used for Search actions where we can recover gracefully and not for content assist and open declaration.

But back to the good news, as we work more on improving the contents of the index I’ll be able to direct all parser operations to it and make the CDT much more responsive for all operations (including my baby – content assist). And even as it is today, there is enough information there for the majority of workflows. Even the field engineers at QNX are extremely happy with it and these are the front line guys who need to make sure their customers are happy. More good news is that I’m getting more help with the indexer, both testing and coding. It’s tough to do this as a one man show and I am appreciating all the help I’m getting from the community.

With the new indexing framework in place in CDT 3.1, the opportunities for exciting new features is wide open. And one of the major objections to using the CDT on large complex projects has been eased greatly. It’s time to get the message out, now that I can lift my head away from the code!


