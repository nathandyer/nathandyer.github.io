---
layout: post
title: Everything You Actually Need to Build a Local Music Collection
summary: Why Pitchfork's recent article about building a local music collection does a disservice to those actually wanting to build a music collection.
---

I recently came across an article on _Pitchfork_ titled ['Everything You Need to Build a Local Music Collection'](https://pitchfork.com/features/article/everything-you-need-to-build-your-own-digital-music-collection/), and despite its seemingly up-beat tone about how great it is to have a local music collection, I would almost swear that some nefarious streaming company paid to have this hitpiece written. I’ve never seen an article give a more convoluted introduction on a new topic for beginners in my entire life.

There are so many reasons why you might prefer a local music collection. You don't have to keep paying a recurring cost to have access to your music. You can play it on any device or player you'd like, not just the ones built specifically for a given streaming surface. You're not being [emotionally surveiled so companies can turn your emotions into raw profit](https://thebaffler.com/downstream/big-mood-machine-pelly). Nobody can reach into your collection and remove something when their contract expires, or when an arist decides they want to shelf an older release, or change their name. None of your money goes to keeping _Joe Rogan_ on the airwaves. You don't have to deal with buffering or rely on expensive data plans. But if you read this article, you don't get any of that context. Instead, you're almost certain to have already run away screaming with your hands in the air, clinging to your _Spotify_ account for dear life.

Here’s the _real_ truth: to build a local music collection, you need a device that can store and play audio files, a device that can output sound, and a file to play.

Or, in other words, you need a laptop/desktop, some headphones, and something to play on them. That’s it. For anyone reading this, odds are good you already have it all.

The article makes it sound like you need a dedicated media server to even get started (they suggest an Intel NUC). They say it’s the “heart” of any digital media collection. Nope! If you’re the laptop-type, you can literally only just ever use your laptop. If you’re a mobile user, you can send files wirelessly to your phones and tablets, or send them across a USB cable if you prefer. 

If you’re the type of person that wants to make the files available to multiple devices in your home, you can enable media sharing out of the box on most systems. In Linux (at least distributions using the GNOME desktop), you go to Settings → Sharing → Media Sharing, and turn it on. Viola! Any devices that support DLNA (which are basically all set top boxes) will be able to see your music automatically without any fussing or making a dedicated server.

You don’t need a NAS to store your files. Unless your collection is in the TBs, which is frankly a metric buttload of music, everything can just live on your laptop/desktop, and can be backed up to whatever disk or cloud service you already use for automated backups.

Unless you’re a really discerning audiophile, you absolutely don’t need a standalone DAC. The built-in DACs on most laptops and phones are pretty great. And let’s be real, most folks will be using a Bluetooth device these days, anyway.

You don’t need a special router, and you don’t need to open stuff up to the internet. Just keep it all with you.

Of course, that’s not to say you *can’t* do things that way. If you want to set up a dedicated media server in your house, by all means, please do. If you want to have everything stored on a NAS to make storing and copying your music easier, of course, you absolutely should! If your ears are sensitive enough to pick out the subtleties of really high-grade headphones and DACs, then go nuts.

But if you’re starting out (which I assume you are, otherwise you wouldn’t be reading that article about how to get started with a local music library), you don’t need any of that crap. Take the laptop you already have, buy some stuff on Bandcamp or Soundcloud (or rip some old CDs lying around), find an app you like, and enjoy. It’s really that simple.

So what do I use and recommend? 

- I have my music library stored a lossless FLAC files (mostly) in the ~/Music folder on my laptop. I use [Lollypop]([https://flathub.org/apps/details/org.gnome.Lollypop](https://flathub.org/apps/details/org.gnome.Lollypop)) to play them.
- I use an app called Doppler on my iPhone. I plug in my iPhone in to my laptop, go to Files → iPhone → Doppler, then copy and paste the music from ~/Music to this location. Once they’re copied, Doppler automatically scans the files and just like that, I have music on my phone, too.
- Back when I used Android, I just copied everything directly to the storage (no need for a special player). That said, I did always like the Phonograph app for playing the music.
- I don’t use it much, but to have the music available on my home entertainment center, I use the built-in media sharing tools inside of Fedora / GNOME that I mentioned earlier (Settings → Sharing → Media Sharing)
- I have a set of AirPods I use for my day-to-day listening, with a nice pair of Sony WH1000-XM3s for when I want to get the best quality I can. For the nerdy among you, I use the LDAC codec to get as good of audio over Bluetooth as I can. Is it as good as a cable? Probably not, but it’s so close that my ears can’t tell a difference.
