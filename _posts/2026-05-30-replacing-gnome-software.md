---
layout: post
title: Replacing GNOME Software
summary: Removing GNOME Software and replacing it with Bazaar is an instant upgrade
date: 2026-05-30 15:00:00 -0400
---

I try to be charitable when it comes to free (libre) software. Most of the tools that I use are made by people who are developing and maintaining them in their free time, with no financial compensation in return. What they do is a gift to the open source community, to the public commons, to the world.

But sometimes my rage overcomes my gratitude, and I can't help but feel frustrated with a tool I'm using. Such is my life working with _GNOME Software_, the application and firmware installation tool.

I've tried, I mean _really tried_, to like GNOME Software. But every time I open it, it freezes, hiccups, or otherwise does something that gets in my way. I often don't even _intend_ to open it in the first place! I'll inadvertently click a .flapakref file, or search for an app that I think is already installed but isn't, and then it leaps to life on its own.

At which point it inevitably locks up and slows down my entire system until it asks if I want to force quit the application, the equivalent of taking it out behind the shed and putting it out of its misery. 

A few weeks ago this happened one too many times, the straw that finally broke the camels back. My frustration grew beyond what I was willing to tolerate. I originally thought that removing it would result in accidentally uninstalling the entire GNOME desktop environment, but to my happy surprise GNOME Software is not a hard dependency, and removing it had no downsides.

I was also worried that removing it would mean I could no longer install firmware updates via fwupd, but I was quite pleased to find there is an official standalone application called "Firmware" that gives you even more access, and it's made by the maintainer of fwupd itself.

With no real downside, and with the knowledge that there is essentially never a scenario where I want to install the RPM version of a package rather than the Flatpak (and for those rare events I can `dnf install` from a Terminal), I purged it completely.

In its place I turned to a software manager (app store?) that I had already grown incredibly fond of, [_Bazaar_](https://flathub.org/en/apps/io.github.kolunmi.Bazaar).

Bazaar is the exact opposite of GNOME Software, and is indeed one of the finest examples that I can point to in regards to the kinds of incredible software that can be made on the modern GTK/Adwaita stack.

The design is immaculate. The animations are fluid and delightful, but never get in your way. It's fun, but also stable and dependable. Everything just works. Bazaar is astonishly pleasant to use. And while it is limited to just the apps available in Flathub, those are the only applications I'm currently interested in installing, so I see that as a benefit more than a limitation.

I hope that one day GNOME Software can improve, or else be replaced by something like Bazaar. I would love to see a future where Bazaar is the default way of installing apps in GNOME, and the system updates and firmware patches are available to install via the settings app, like many other modern OSes. I've seen some early plans pointing in that direction, so I'm hopeful.

Until then, I will make do using Bazaar and Firmware, and manually install OS updates through the Terminal. Using three tools instead of one is not quite a replacement, but it is infinitely less frustrating.
