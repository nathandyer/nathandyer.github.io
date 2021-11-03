---
layout: post
title: Improving the Linux Bluetooth Experience
image: /img/bluetooth/banner.png
summary: The world has moved to Bluetooth, and the experience on Linux is better than ever — with a few minor changes.
---

![A hand-drawn banner that reads "Bluetooth in Linux", with the Bluetooth symbol]({{ site.url }}/img/bluetooth/banner.png)

For quite some time I've [complained](https://twitter.com/nathandyer_/status/1406374368817655815) about the [Bluetooth experience](https://twitter.com/nathandyer_/status/160171088138088449) on [Linux-based systems](https://twitter.com/nathandyer_/status/103618889765752832) (not including Android), but recently I've come across a few methods of improving the quality of life of using Bluetooth devices on my Linux systems, and I wanted to share some of the tips and tricks I have learned with the wider community.

For a brief background on my set-up and the types of devices I regularly connect to my systems, about a year ago I decided I wanted to go all-in on Bluetooth, so every peripheral that I connect to my system is using Bluetooth. My keyboard (Keychron K3) is Bluetooth. My travel mouse is Bluetooth. For audio, I use either AirPods Pro ear buds, Sony WH-1000XM3 headphones, or a JBL Flip 5 portable speaker. I sometimes connect an Xbox controller, as well as an 8BitDo SNES-esque controller. Pretty much across the board, if it connects to my system, it's wireless, and done through Bluetooth.

So, without further ado, here are my recommendations:

## 1. Install the Bluetooth Quick Connect extension (GNOME)

![A screenshot of the Bluetooth Quick Connect extension, which lists out various paired Bluetooth devices]({{ site.url }}/img/bluetooth/quick-connect.png)

I generally recommend against installing extension in GNOME Shell, but this one is absolutely critical for my sanity. Rather than clicking the Bluetooth icon in the top right and then having to go to the Settings application to select and connect to a device (which often involves repeatedly clicking or tapping the connect switch, as it times out and goes back to the "off" state without a retry), I can just see a list of my paired devices, and do a single click to connect.

You can find and install the Bluetooth Quick Connect extension by opening the following link in either Firefox or GNOME Web
[https://extensions.gnome.org/extension/1401/bluetooth-quick-connect/](https://extensions.gnome.org/extension/1401/bluetooth-quick-connect/)

## 2. Disable notifications for every Bluetooth connect and disconnect event

Bluetooth event notifications almost did me in. For months, every single time my keyboard reconnected after going into a low-power state, every time my mouse had a brief connection hiccup, every time I placed my AirPods in or out of my case, I would be treated to at least one, if not multiple, notifications letting me know that something had changed.

Perhaps this is just me (although I don't think so, as most other OSes don't seem to use this either), but I don't need notifications to know when a device connects or disconnects.

If I'm listening to music and my headphones disconnect, my music stops playing. It doesn't pass by without notice.

Likewise, if I go to type on the keyboard and it doesn't type, I don't need something to tell me that it's not connected. 

I tried disabling these notifications from the system Notifications settings, but nothing I did could stop them from coming.

Finally, I discovered that they can be disabled by installing the Bluetooth Manager application (which you can find in the Software Center / AppCenter / Pop!_Shop, or by installing the `blueman` package from the Terminal on most distributions), and then going to View -> Plugins -> ConnectionNotifier, and un-checking the box.

![A screenshot of where to disable notifications in the Bluetooth Manager (Blueman) app]({{ site.url }}/img/bluetooth/blueman-notifications.png)

## 3. Make the switch to PipeWire

This one is specific to audio devices, but I have historically had a fairly miserable experience with audio devices in Linux over Bluetooth.

Ever since Fedora has switched to PipeWire, though, the experience has been so much better.

With few exceptions, when I now connect a Bluetooth device, the audio gets routed to it properly, and I don't have to go in and configure anything.

When I remove the AirPods from my ears, the sound pauses, and when I click resume, it automatically picks back up with my integrated speakers (in the case of my laptop).

What's also great is, instead of only using the standard A2DP codec (which is very lossy), on headsets that support other codecs, it automatically chooses higher-quality, less-lossy formats (such as AAC on my AirPod Pros, and aptX HD or LDAC on my Sony headphones).

The experience of using PipeWire instead of PulseAudio is night-and-day, and I cannot recommend it highly enough. 

The best way to use PipeWire is to use an OS that uses it by default (such as the newly-released [Fedora 35](https://getfedora.org/workstation/download/)), but you can find instructions for installing and enabling it on most distributions here: [https://pipewire.org/](https://pipewire.org/)

## 4. Use a well-supported Bluetooth adapter

This one is a bit of a given, but it's worth mentioning, because a good Bluetooth experience only starts with a well-supported Bluetooth adapter.

For best results, I recommend using an Intel-based wireless adapter, with Bluetooth built-in. The performance is great, they're well-tested, and the drivers are built directly into the kernel.

For laptops or systems that you purchase pre-configured, the best advice is to purchase from a company like [System76](https://system76.com/) that specializes in such hardware (disclaimer: I work for System76 on the Happiness Team provided customer support), or use a brand that is used by a large portion of Linux developers (when in doubt, ThinkPads tend to work very well because so many developers use them). 

# Wrap-Up 

If you try any of those suggestions, or if you have any other suggestions for improvement, I'd be really curious to hear about your experience! Please reach out to me via [Mastodon](https://fosstodon.org/@nathandyer), [Twitter](https://twitter.com/nathandyer_), or [Email](mailto:nathandyer@fastmail.com)! 