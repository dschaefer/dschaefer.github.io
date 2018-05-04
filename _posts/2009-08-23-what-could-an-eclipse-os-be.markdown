---
layout: post
title: What could an Eclipse OS be?
date: '2009-08-23 19:27:00'
---


I got some really positive feedback on my quick little demo of the “Eclipse OS” prototype that I’ve started building. So I’ve started to capture ideas on the github wiki for the repository that I created there. Feel free to add your thoughts there, or here. Maybe if there’s enough interest we could grow a little community around the idea. If not, that’s fine too. I’m really just exploring a role Eclipse technologies could play in a browser based “OS” such as the announced Google Chrome OS.

Here’s the link to the wiki and here is what I’ve started with: [http://wiki.github.com/dschaefer/eclipseos](http://wiki.github.com/dschaefer/eclipseos)

What should the Eclipse OS be? Take one of those new fancy 10″ netbooks. Install enough Fedora to xinit the Google Chrome browser with the Flash plugin (necessary in my books for a full web experience) and launch an Equinox standalone server. What local web applications would you need to manage your netbook? Feel free to add to this list.

- Power Off. To shutdown the OS and power down, i.e. run the poweroff command. (Update: this is the first app and is now working).
- Install Manager. To install new web apps into the server using p2. Integrate p2 with yum to install native components that the web apps may need.
- Audio Manager. Similar to ALSA mixer but as a web app. To control the volume of the audio in the least. This could be a good first test of writing native code to help implement the service.
- File Manager. To look at and manipulate the files on the system, maybe even open them in the browser.
- Connectivity Manager. To manage wireless and wired network connections.
- Power Manager. To manage power saving modes.
- Office “Suite”. To prepare documentation and presentations while disconnected, like on long flights.
- E-mail. For those who would like offline access to e-mail.
- An IDE so I can build my web apps locally (thus the connection with my Web IDE (W-IDE) prototype).


