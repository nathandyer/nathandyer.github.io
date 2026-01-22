---
layout: post
title: "HandBrake "
date: 2010-09-09
tags:
  - Blu ray ripping
  - Blu-ray
  - DVD ripping
  - Handbrake
  - MP4
  - Ogg Theora
  - video encoding
categories:
  - Mac
  - Operating Systems
  - Other Linux Distros
  - Ubuntu
  - Video Editors/Encoders
  - Windows
---

<a href="http://ossftw.wordpress.com/wp-content/uploads/2010/09/screenshot-handbrake.png"><img class="alignleft size-medium wp-image-378" title="HandBrake" src="http://ossftw.wordpress.com/wp-content/uploads/2010/09/screenshot-handbrake.png?w=300" alt="" width="300" height="202" /></a>

HandBrake has often been billed as the best DVD-ripper in the world, especially by Mac users. I bill it as the best video encoder that has ever been created. I first became introduced to this software back in my Windows years, and found that the program was not firing on all cylinders. Fast-forward a few years, and you have one of the most reliable, stable pieces of software around, with more-than-capable versions for all the major operating systems.

It's the most powerful encoder I've used for several reasons. Let me say, first, that it doesn't exactly convert to many file formats. In all honesty, though, I only use MP4 (with the .m4v extension). I know that, since this is a blog about open-source, you would imagine that I would be all for using Ogg Theora. Honestly, I hate it, and can't wait for it to die. The compression is the worst of any video format I've ever seen- even WMV.

Video codec rant aside, HandBrake is awesome. The idea is simple: either stick in a DVD, or select the location of the video file. After a brief scan (takes like 2 seconds), you'll be able to tinker as much as your heart desires. I've spent days out of my life experimenting with the different options, and I now have it down to a science. I encode everything in a MP4 with AAC audio at 320 kbps, using MPEG4 video at whatever bitrate the original is- typically, for DVDs, around 1000 kbps. I don't embed subtitles, because I don't use them and they often automatically load when a video begins playing, but at times I do include chapter marks. And I always leave the box marked "Large File Size &gt;4 GB" checked. Just a tip if you want to make big videos.

There are additional features you can use at your own risk, including H.264 filters and manual cropping (which HandBrake does automatically). I've yet to see an encoder with as many options as this. I don't expect to convince you with that, so let me give you an example of how powerful this can be. Last night I ripped a Blu-ray using MakeMKV, imported that ripped file into HandBrake, and in relatively no time I had a beautiful, shrunken copy with two different audio tracks (a stereo track @ 320kbps, and a 5.1 channel track at ~720kbps). You can put in all or nothing, but I managed to get a fantastic result weighing in at just under 17 GBs.

Honestly, this is great software, and because it's free, it's not like you have anything to lose. I mentioned on Twitter about software being a work of art: this is it. Hundreds of features, packed into a simple program with great layout and GUI. Download now.
<h4>Stop the presses! Friend of the blog technologyunit posted a great video guide to installing and using HandBrake on his blog. If you're interested, you can catch a gander <a href="http://ubuntuvideotutorials.org/2010/07/13/trancode-video-in-ubuntu-with-handbrake/">here</a>.</h4>
<h2>Downloads</h2>
<h3><a href="http://handbrake.fr/rotation.php?file=HandBrake-0.9.4-MacOSX.5_GUI_x86_64.dmg"><img class="alignleft size-full wp-image-35" title="Mac OS X" src="http://ossftw.wordpress.com/wp-content/uploads/2010/07/b6d767d2f8ed5d21a44b0e5886680cb9-apple-logo-256x256.png" alt="" width="52" height="52" /></a><a href="http://handbrake.fr/rotation.php?file=HandBrake-0.9.4-Win_GUI.exe"><img class="alignleft size-full wp-image-38" title="Windows" src="http://ossftw.wordpress.com/wp-content/uploads/2010/07/windows_logo.png" alt="" width="52" height="52" /></a><a href="https://edge.launchpad.net/~stebbins/+archive/handbrake-snapshots/+build/1952429"><img class="alignleft size-full wp-image-36" title="Ubuntu" src="http://ossftw.wordpress.com/wp-content/uploads/2010/07/cof_orange_hex.png" alt="" width="52" height="52" /></a><a href="https://edge.launchpad.net/~stebbins/+archive/handbrake-snapshots/+build/1952428"><img class="alignleft size-full wp-image-39" title="Ubuntu x64" src="http://ossftw.wordpress.com/wp-content/uploads/2010/07/cof_black_hex.png" alt="" width="52" height="52" /></a><a href="http://handbrake.fr/rotation.php?file=HandBrake-0.9.4.tar.bz2"><img class="alignleft size-medium wp-image-37" title="Other Linux Distros (Source Code)" src="http://ossftw.wordpress.com/wp-content/uploads/2010/07/tar-gz.png?w=300" alt="" width="52" height="52" /></a></h3>