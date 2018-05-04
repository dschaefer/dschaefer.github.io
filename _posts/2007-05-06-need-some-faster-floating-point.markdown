---
layout: post
title: Need some faster floating point?
date: '2007-05-06 08:23:00'
---


As I mentioned a couple of days ago, my new hobby is raytracing. I have a curious mind (in more ways than one 🙂 and I always wonder how computers do the things they do. So when my sons got old enough to enjoy video games, we started down that path, and, of course, my curiosity lead me into the world of game programming. In order to make games look good, game programmers use a lot of tricks and play with optical allusions a lot. It’s pretty complicated and every time I tried to get into it more, the real world would pull me out and make me deal with it.

In researching [my recent blog entry on raytracing](http://cdtdoug.blogspot.com/2007/04/ray-tracing-future-of-gaming.html), I found a sweet elegance that I always look for in computer architectures. The algorithms are pretty straightforward, albeit pretty compute intensive, so the barrier to entry into this area seems low enough that I can work on it when I get a chance. It also looks to benefit immensely from parallel processing, another interest of mine, and will get me into that area as well. That, and the demos I saw showed some wicked shadow affects that really added to the realism of scenes, so it’ll be cool to show off as a CDT demo as well (as opposed to the [spinning polygons](http://nehe.gamedev.net/lesson.asp?index=01) I use as an SDL/OpenGL demo right now that you may have seen at ESC).

My first step was to build a vector class that does math with 3D vectors, a critical component of all graphics programming. The sample I was looking at used regular C++ floating point arithmetic with a vector composed of a float for each of the three axis.

  
<span> class vector {</span>  
<span> public:</span>  
<span> vector(float _x, float _y, float _z)</span>  
<span> : x(_x), y(_y), z(_z) { }</span>  
<span> void operator +=(const vector & v) {</span>  
<span> x += v.x; y += v.y; z += v.z;</span>  
<span> }</span>  
<span> private:</span>  
<span> float x, y, z;</span>  
<span> };</span>  
<span></span>

Pretty basic. But this is the first example of an algorithm that can benefit from parallelism. Since I have a fairly new laptop, I wondered if I could leverage [SSE, Streaming SIMD Extensions](http://en.wikipedia.org/wiki/Streaming_SIMD_Extensions) to implement this. I also wondered how well gcc and the MinGW variant I’m using handles SSE. So I gave it a try.

  
<span> class vector {</span>  
<span> public:</span>  
<span> vector(float _x, float _y, float _z) {</span>  
<span> float array[4] __attribute__((aligned(16)))</span>  
<span> = { x, y, z, 1 };  
 xyz = _mm_load_ps(array);</span>  
<span> }</span>  
<span> void operator +=(const vector & v) {</span>  
<span> xyz += v.xyz;  
 }  
</span><span> private:</span>  
<span> __m128 xyz;</span>  
<span> }</span>  
<span></span>

The constructor is a bit more complicated. And with most things dealing with SSE, 16 byte alignment is critical for good performance. And looking at the generated assembly, I was pleased to see that gcc, after making sure I put the -msse2 option on the compile, worked hard at keeping the instances of __m128 aligned like that. The performance tests I ran with addition showed an O.K improvement in performance, especially as the number of math operations grew. But when I tried multiplication instead of addition, the performance gains were astronomical. Well worth the extra typing.

Now that I’ve got that under my belt, I can’t wait to actually draw something…


