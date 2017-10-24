---
layout: post
title: 'Vocal Development Update #2'
---
The past week has been primarily focused on completing my final projects for courses this semester, but tonight I turned in my last two projects. I can finally start focusing on Vocal 100%.

Despite focusing on school assingments, I still managed to make a fair bit of progress with Vocal. The main improvement is that album art now rearranges itself properly when the window shrinks or grows! [The screencast that I recorded (sorry, no audio)](https://www.youtube.com/watch?v=AiKGJaYGuhg) should give you a good idea of how Vocal looks and behaves right now.

I initially started out with my own custom widget in a Grid, and threw in some voodoo on the backend to make it work, but I couldn't find a good solution to fixing the resize problem. So in the end I decided to try a Gtk.IconView, and in only an hour or two I had it looking and working exactly how I wanted. Awesome!

There was some additional work on the parser to make it be able to detect audio vs. video. I also started working on integrating video, and have had some success. Vocal is actually able to play video right now, but the experience is nowhere near what I want it to be. I'm going to set that aside for now while I implement more critical features.

For the next few days I am going to work on cleaning up some of the code, fixing a few minor issues, and getting Vocal into a relatively stable state with its current minimal functionality.

And then, the library management.
