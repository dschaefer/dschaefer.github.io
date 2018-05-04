---
layout: post
title: Debugging Vert.x apps with Eclipse
date: '2012-05-15 21:44:00'
---


+Pascal Rapicault has me hooked on Vert.x, http://vertx.io. It looks like it can be a great competitor to node.js allowing you to use the same asynchronous web programming model not only with JavaScript by any of your favorite JVM languages, including Java believe it or not!

At any rate, tonight I started to see if I can use Eclipse to develop apps in Vert.x. It turned out to be a lot trickier than I thought so I figured I’d capture what I did here.

First, you need to create a User Library for Vert.x. I just looked at the bin/vertx script to see what it added to the Java classpath to see what jars to add to the library. After that I was able to create a Java project and add the library to the build path and code up my little hello world app (which indeed is very node.js like).

<div>[![](http://4.bp.blogspot.com/-_zcsyw_aezM/T7MS8vIL1kI/AAAAAAAAAZM/t-P2-n8uAz8/s320/Screen+Shot+2012-05-15+at+10.36.53+PM.png)](http://4.bp.blogspot.com/-_zcsyw_aezM/T7MS8vIL1kI/AAAAAAAAAZM/t-P2-n8uAz8/s1600/Screen+Shot+2012-05-15+at+10.36.53+PM.png)</div>Launching is pretty tricky. First, Vert.x doesn’t want your app to be on the classpath when it starts up. Weird and that means you have to remove your project from the Classpath. But you do then need to add in your Vert.x user library using the advanced option so it can launch Vert.x’s main, which is VertxMgr.

<div></div><div>[![](http://3.bp.blogspot.com/-eGXd72i6p50/T7MT10-3ZqI/AAAAAAAAAZU/6z-CagQgy7I/s320/Screen+Shot+2012-05-15+at+10.39.06+PM.png)](http://3.bp.blogspot.com/-eGXd72i6p50/T7MT10-3ZqI/AAAAAAAAAZU/6z-CagQgy7I/s1600/Screen+Shot+2012-05-15+at+10.39.06+PM.png)</div><div>[![](http://4.bp.blogspot.com/-LjdllaOmX_k/T7MT_GNsalI/AAAAAAAAAZc/HjiOAwL6wZI/s320/Screen+Shot+2012-05-15+at+10.38.36+PM.png)](http://4.bp.blogspot.com/-LjdllaOmX_k/T7MT_GNsalI/AAAAAAAAAZc/HjiOAwL6wZI/s1600/Screen+Shot+2012-05-15+at+10.38.36+PM.png)</div>And you need to add your project build output with the -cp application option, which I passed ${project_loc:/vertxHelloWorld}/bin, so it can find your Verticle class.

<div></div><div>[![](http://3.bp.blogspot.com/-UV5k1x8uf9Y/T7MUEqa741I/AAAAAAAAAZk/FdzwLKn0-NI/s320/Screen+Shot+2012-05-15+at+10.38.49+PM.png)](http://3.bp.blogspot.com/-UV5k1x8uf9Y/T7MUEqa741I/AAAAAAAAAZk/FdzwLKn0-NI/s1600/Screen+Shot+2012-05-15+at+10.38.49+PM.png)</div>Finally when you debug, the Default source path matches your Classpath. Since you removed your project from the Classpath, you have to add your project to the sources manually in the Source tab.

<div>[![](http://2.bp.blogspot.com/-bdOKFmbWvvM/T7MUJUxNHLI/AAAAAAAAAZs/L_0veP9zEg4/s320/Screen+Shot+2012-05-15+at+10.39.27+PM.png)](http://2.bp.blogspot.com/-bdOKFmbWvvM/T7MUJUxNHLI/AAAAAAAAAZs/L_0veP9zEg4/s1600/Screen+Shot+2012-05-15+at+10.39.27+PM.png)</div>I imagine someday, someone will create a Launch Configuration that will do this all for you but if you put some muscle in it, you can get up and debugging your Vert.x app in Eclipse now. Now, if I can debug my client-side JavaScript in the same session…

<div></div>
