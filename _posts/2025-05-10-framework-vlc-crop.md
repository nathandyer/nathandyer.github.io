---
layout: post
title: Cropping videos in VLC to 3:2 for the the Framework display
summary: A short explainer of how to add a custom 3:2 crop option so video will fill your Framework display
---

Here's a little pro-tip I discovered in VLC, which will allow you to crop your videos to a 3:2 aspect ratio that matches the display in the Framework laptop.

This works best on videos that are either 16:9 or 4:3 aspect ratio to begin with. For really wide theatrical videos (like 2.35:1) you will lose too much of the picture for this to be worth it, but for videos that are vaguely Framework-shaped, it might be worth shaving off a bit of the content so you can use every square inch of your display.

To do this, in VLC, go to Preferences → Show settings → All, then navigate to Video → Custom crop ratios list, and add the text “3:2”. When you’re done, click Save.

After that, when you load a video, you can now select to crop to 3:2 from the Video → Crop menu, and when you go fullscreen it will use the full display.

![]({{ site.url }}/img/framework-vlc.jpg)

(Note: I originally posted this to the Framework community via [this post](https://community.frame.work/t/pro-tip-cropping-videos-in-vlc-to-take-advantage-of-the-framework-display/67771))
