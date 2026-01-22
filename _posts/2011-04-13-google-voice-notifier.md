---
layout: post
title: "Google Voice Notifier"
date: 2011-04-13
tags:
  - Google Voice
  - notifier
  - ubuntu messaging menu
categories:
  - Social
  - System Tools
  - Ubuntu
---

I wanted to share a quick post about a piece of software I found that has saved me tons of aggravation and has made my life about a billion times simpler. As a seventeen-year-old part-time fast-food worker/blogger, I'm a little strapped for cash, so I have relied on Google Voice for my texting and audio needs for quite a while.

<img class="alignleft" title="Google Voice Icon" src="http://www.wired.com/images_blogs/epicenter/2011/01/2009-07-15_google_voice_fluid_preview.png" alt="" width="122" height="122" />

For those of you who don't know, <a href="http://voice.google.com/" target="_blank">Google Voice</a> is a service that allows you to <a href="http://www.google.com/support/voice/bin/static.py?page=guide.cs&amp;guide=1086099#utm_source=hc_header&amp;utm_medium=GettingStarted&amp;utm_campaign=homepage" target="_blank">send SMS messages and make some calls for free (that's a simplified explanation).</a> The only problem that I've had is that I needed to fire up a browser and hit refresh to check for new messages.

<a href="http://ossftw.wordpress.com/wp-content/uploads/2011/04/screenshot-1.png"><img class="alignright size-full wp-image-562" title="Google Voice Messaging Menu" src="http://ossftw.wordpress.com/wp-content/uploads/2011/04/screenshot-1.png" alt="" width="229" height="151" /></a>Now there's an app for Ubuntu (and Ubuntu-based variants, I would imagine) that ties directly into the messaging system. It turns the little envelope blue when you get a new text message, and lists the number that contacted you. This way, I get a desktop notification and never have to miss an important text message or voicemail again!
<h3>Download/install</h3>
You can install by running the following in the terminal:
<pre> sudo add-apt-repository ppa:ken-vandine/notifiers
 sudo apt-get update
 sudo apt-get install gvoice-notifier</pre>
To report bugs or ask questions, visit the <a href="https://launchpad.net/gvoice-notifier" target="_blank">Launchpad page</a>