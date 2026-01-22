---
layout: post
title: "How to Properly Encode WebM Videos from DVDs and Blu-rays"
date: 2011-06-25
tags:
  - blu-ray
  - encode
  - ffmpeg
  - Linux
  - Open Source
  - rip blu-ray
  - Ubuntu
  - video codec
  - VP8
  - WebM
categories:
  - Computers
  - Linux and Open Source Software
  - Other Software/Applications
---

<a href="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/webm-logo1.png"><img class="alignleft size-medium wp-image-539" title="WebM, an open-source video container (VP8 video + Ogg Vorbis Audio)" src="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/webm-logo1.png?w=300" alt="" width="300" height="68" /></a>WebM is an open source video format, designed to be a good and royalty-free alternative to H.264. It's been around for nearly a year now, and while adoption is growing, it's still not well-known how to encode or use these types of videos. I've spent days upon days monkeying around, and I'm here to show you how to do it properly, as not to drive you absolutely crazy.

<strong>Important note</strong>: I am using ffmpeg inside of Ubuntu 11.04. Your mileage may vary, but the processes I detail should work the same for all installations of ffmpeg.
<h2>Getting Started</h2>
The first order of business is getting your video. Most likely, <span style="text-decoration:underline;">assuming you're wanting to do it only for making backups of the content you paid for and own</span>, your content is stored on either a DVD or Blu-ray. <strong>Note</strong>: if you want to rip Blu-ray discs, you MUST have a Blu-ray drive installed on your machine.

I recommend using <a href="http://www.makemkv.com/download/" target="_blank">MakeMKV</a>. It's considered a paid-for application if you want the Blu-ray support, but it's completely free while it's in Beta (I've used it for two years, and it's been in beta the entire time, so it's unlikely you'll have to pay for a while). Whenever the trail version expires, just jump over to the <a href="http://www.makemkv.com/forum2/viewtopic.php?f=5&amp;t=1053" target="_blank">website and get the new Beta key</a> for that month.

Follow the download instructions, then run MakeMKV. Note: in Linux, you'll likely have to open a terminal and type 'makemkv'.

<a href="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/makemkvopen.png"><img class="alignleft size-thumbnail wp-image-545" title="MakeMKV First Run" src="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/makemkvopen.png?w=148" alt="" width="148" height="150" /></a>Once the program loads, press the middle button (with the image of a disc to hard drive), and allow it to circumvent the copy protection.

<a href="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/makemkv-run.png"><img class="alignright size-medium wp-image-547" title="MakeMKV TItle Select" src="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/makemkv-run.png?w=300" alt="" width="300" height="255" /></a>

&nbsp;

&nbsp;

&nbsp;

It will then list all the titles on the disc. Find the one that contains the movie (generally the largest one), and drop down the menu. Select the first audio track (assuming that it's the one you want), and make sure all other options are not selected (other titles, subtitles, and other audio options. Especially other audio options). Then point it to a location on your hard disk (default is in your video folder), and press the "MakeMKV" button. Now take a pee break, grab a soda, and let it do its thing.
<h2>Using FFmpeg</h2>
The next part requires using FFmpeg, a command-line (terminal) based program to convert media. If you're using Ubuntu or any of the derivatives. you can use
<pre>sudo apt-get install ffmpeg</pre>
A windows version can be found <a href="http://www.videohelp.com/download/FFmpeg-git-N-30656-g23a29a3.7z" target="_blank">here</a>. To open the 7-zip package you may need to install <a href="http://www.7-zip.org/" target="_blank">the 7-zip software</a>.

Otherwise, <a href="http://www.ffmpeg.org/download.html" target="_blank">you may have to compile it.</a> You likely know how to do so, but if not,<a href="http://lmgtfy.com/?q=Compile+ffmpeg+from+source" target="_blank"> there are plenty of guides.</a> Once you have ffmpeg installed, open your terminal (Mac or Linux), or your command prompt in Windows. <strong>Please note:</strong> I've not used the windows version, and as such the instructions may be completely different, and the following will be of little to no use for you. If that's the case, I apologize. <strong>The following will work in Linux and Mac.</strong>

The command that I use is as follows, and I'll elaborate in a moment:
<pre>ffmpeg -i '/home/nathan/Videos/example.mkv' -ab 192k -ac 2 -vcodec libvpx -aspect 16:9 -async 2 -b 5500k -minrate 4500k -metadata title="Example" example.webm</pre>
I'll go through all the commands piece by piece to show you exactly what I configured:
<ol>
	<li>ffmpeg: tells the terminal to launch the program 'ffmpeg'</li>
	<li>-i: tells FFmpeg that the path following the '-i' switch is the input video.</li>
	<li>'/home/nathan/Videos/example.mkv': the path to the input video file. You can drag the video file to the terminal and it will add the path automatically.</li>
	<li>-ab 192k: sets the audio bitrate for 192 kbps. You can select another value (examples: 128 for low size, 256 or 320 for very high quality)</li>
	<li>-ac 2: <strong>Extremely important!</strong> This ruined many of my early encodes. FFmpeg has problems with the AC3, 6-channel audio most DVDs have, and without this switch, it produces a loud whine for an audio track on the output. This tells ffmpeg to downmix to 2 channels of audio.</li>
	<li>-vcodec libvpx: Also very important. This tells FFmpeg that you're using libvpx to create your video. It encodes it in VP8 video and Ogg Vorbis audio, part of the WebM container standard.</li>
	<li>-aspect 16:9: tells FFmpeg to keep your video in the Widescreen format. I only had to do this for DVDs, but it was very important. <span style="text-decoration:underline;">If your video is a 4:3, then you'll change it to '-aspect 4:3'.</span></li>
	<li>-async 2: I had a problem with the audio and video being out of sync, especially towards the end of videos encoded from DVDs. This tells FFmpeg to make sure the audio stays in sync. You might can skip this for Blu-ray encodes.</li>
	<li>-b 5500k: <strong>This is super important.</strong> This is where you set your bitrate for the video. The higher the bitrate, the better the quality, and the higher the file size. DVDs are encoded at ~5000 kbps, so if you want to maintain that quality, you should set it for nearly the same. Note that this will typically create around a 4GB file. Set it for a lower number to reduce the size of the file. <strong>For Blu-ray encodes, the number is much higher. It can be as high as 30000k, but for a nice mix between size and quality, I would do between 10000-12000 kbps.</strong></li>
	<li>-minrate 4500k: This tells FFmpeg to try to make sure that it never drops below 4500 kbps while encoding, to maintain a consistent quality. This number should be about 500-1000 lower than your bitrate. You don't <em>have</em> to set a minimum bitrate, but I've found it well worth my time to do so.</li>
	<li>-metadata title="Example": Completely optional. This sets the metadata for the video. In this example, it tells it that the title is 'Example.' You could add artist, album, or year to the information, as well as any comments.</li>
	<li>example.webm: Tells FFmpeg where to save the output file, and that it will be using the WebM format. In this instance, it will place the output in my home folder in a file called 'example.webm'. You could also specify a path, like '~/Desktop/Example Season 1/Example.webm'</li>
	<li><strong>FOR BLU-RAY ENCODES</strong>: you may wish to specify output frame size. If you want 1080p you wouldn't have to, but if you wanted to just create a 720p video, you could add:</li>
</ol>
<pre>-s 1280x720</pre>
After running those commands, let FFmpeg do its thing. You can watch it encode, and from time to time I would recommend making sure it isn't doing anything stupid, like dropping your bitrate to the floor.
<h2><a href="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/screenshot1.png"><img class="aligncenter size-medium wp-image-561" title="FFmpeg while encoding" src="http://nathandyer.wordpress.com/wp-content/uploads/2011/06/screenshot1.png?w=300" alt="" width="300" height="195" /></a></h2>
<h2>Viewing Your File</h2>
Once the encode is finished, close the terminal. If you're using Linux, it's likely that you have the ability to playback WebM videos natively. Just locate the file and try to open it, or open it from your video player of choice. In the Mac and Windows worlds, you can use <a href="http://www.videolan.org/" target="_blank">VLC</a> to play the video. Or, if you're a Windows user, you can <a href="http://www.afterdawn.com/software/audio_video/codecs/webm_vp8_directshow_filters.cfm" target="_blank">add WebM support to Windows Media Player/Media Center here</a>.
<h2>Wrap-Up</h2>
That's all there is to it! It may seem like a complicated process, but it's not too bad. When it's all done, you have a video that not only looks and sounds good, but is open source and royalty-free. Without a doubt, we need an open standard, and the Ogg Theora format wasn't cutting it. WebM is a great option, and I look forward to seeing how well it gets implemented and how often it gets used. Good luck!