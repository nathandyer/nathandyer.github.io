---
layout: post
title: Gapless vs. Euphonica
summary: Comparing two modern music players for GNOME/Linux
date: 2026-02-23 20:00:00 -0500
---

Every music player I have tried on GNOME is lacking in one area or another. Since my perfect music player doesn't exist, I thought it might be of interest to say what I do and don't like about the two primary apps that I tend to jump between: Euphonica and Gapless.

Generally, I prefer Euphonica. As someone who likes to listen to entire albums from start to finish, I find that viewing an album and queuing it up for play is a much better experience there. 

I also prefer its "now playing" screen. I love that it tells me the quality details about the song I'm listening to. I like that I can shuffle directly from it, and even adjust features like crossfading and ReplayGain. Plus, I like the larger album art. I could take or leave the audio waveforms, but they are a nice touch.

![A screenshot of the Now Playing screen in Euphonica, showing the items mentioned above]({{ site.url }}/img/euphonica_screenshot.png)

It's also nice that you can set cover art for an entire playlist.

The thing I dislike most about it is the fact that it requires an mpd server to work. I suppose most folks who use Euphonica are connecting to an mpd sever remotely, but I've set one up locally on my laptop (only available to `localhost`) purely for using with Euphonica. It was a small pain to set up, but what really annoys me about it is that it's not always consistent about finding or displaying music that _should_ be available. Occasionally songs or albums will be invisible from the library, but they're so few and far between it's hard to catch. In some cases I'll realize an album is missing, but if I look at it through the artist view and then look at the individual songs list, I'll find an entire album's songs without the album showing up in the list. I suspect this is a shortcoming of Euphonica itself rather than mpd, but because the two are so intrinsically linked, it would take a decent amount of investigation to figure out.

I also miss being able to just see a flat-out list of every song in my library. I often just like to shuffle through everything, and I've not yet found a way to do so here.

Gapless, on the other hand, is a lot more minimal. This is both good and bad. I like that it just pulls from your local music library and handles all that functionality itself without requiring a separate server. So far it has reliably pulled in all my music. It automatically detects my saved playlists in a standard format. The music playback is great.

It's also wicked fast. It launches almost instantly, playback happens as soon as you click play, and navigating the library has no delays.

It's just missing the little bells and whistles that I mentioned that I like about Euphonica: the larger album art, the quality/format details, the shuffle buttons, the individual album views, etc.

![A screenshot of the Now Playing screen in Gapless, for comparison]({{ site.url }}/img/gapless_screenshot.png)

But what bothers me the most about Gapless is the way that it handles the concept of a queue. When you play an album it pulls those tracks out of a queue, but still shows every song in your library within it. If you try to shuffle all your tracks but then play an album, it's like it un-shuffles just the songs from the album, so in the middle there will just be 15 songs by the same artist in album order. 

Sometimes playing individual tracks will clear the queue. Sometimes it appends. It's just confusing to me, I simply don't comprehend how the queue functions. The only time the queue behavior makes sense to me is when I'm playing music from a playlist.

If I could, I'd merge the best of both apps together. I feel like each excels in the exact ways the other falls short, so together it's a complete experience.

Realistically, I think if Gapless were to make just a few tweaks it would be a perfect app. Whereas I think Euphonica, while my current favorite, is more fundamentally flawed in its library management.

Still, I really like both apps, and use them every single day. Maybe one day I'll give up on one and settle on a single tool. Today is not that day, though.
