---
layout: post
title: Fixing Buffering Issues in Kodi While Playing Media from Local Network
---

I know that most people tend to rely on streaming media services these days for their entertainment needs, but having my own private, local media collection is something I have always been obsessed with, and old habits die hard. I almost exclusively watch my own painstakingly ripped, re-encoded, and catalogued Blu-rays and DVDs, which I have stored on a NAS in my house. I then stream the content using Kodi, which I currently have running using LibreELEC on a Raspberry Pi 4 (which I must say is a surprisingly capable home media center solution) connected to my 4K TV.

This has worked well for me for the most part, however for a long time I have been plagued by buffering issues. I use relatively high bitrates for all my media, and with my original configuration my content would often play for a minute or so, then stop, wait for it to catch up a bit, and then start playback again.

I finally decided that this was a solvable problem, so I dedicated some time recently to researching this issue and testing some fixes. After the two following changes, I'm happy to report that I have completely eliminated this problem! 

First, I found out that because I was mounting a Samba share, Kodi wasn't actually treating this content as a normal web stream, and wasn't caching the content correctly. Fixing that was as simple as creating an advancedsettings.xml text file, and saving it in the kodi user's home directory on my Raspberry Pi, at this location: /storage/.kodi/userdata/ (depending on your installation, this may vary; see [this link on the Kodi wiki for full details](https://kodi.wiki/view/HOW-TO:Modify_the_video_cache).

This is a copy of my advancedsettings.xml file:

    <advancedsettings>
      <cache>
        <buffermode>1</buffermode>
        <memorysize>157286400</memorysize>
        <readfactor>1.5</readfactor>
      </cache>
    </advancedsettings>
    
This tells Kodi to buffer content from all sources and filesystems, tells it to use ~150MB of memory for the cache (which requires a total of ~450MB of free RAM at any given time to work correctly), and sets its read rate for 1.5 times the playback rate (so if your media is ~10Mbps, it reads ahead 15Mbps, so your cache is always more full than you strictly require at any given time).

Those changes immediately fixed the buffering issues, however after doing this it introduced a new problem: certain media files would cause Kodi to stop playback immediately after starting (it would play for about one second, then act like it was done).

To fix this, I configured NFS instead of Samba on my NAS and switched to using NFS instead. That immediately cleared up this issue! Between switching to NFS and adding this advancedsettings.xml configuration file, playback is essentially flawless!

Hopefully that information will be helpful to someone else. If you're experiencing similiar buffering issues with Kodi while playing content on your local network, give those changes a try and see if you notice an improvement!
