---
layout: post
title: A Short Review of the JBuds Ergo Mouse in Linux
summary: It's a really great mouse for under $40
date: 2026-02-05 20:00:00 -0500
---

While I was at my local big box electronics retailer store recently, I stumbled across a relatively inexpensive vertical mouse that I was unfamiliar with. I have a Logitech Lift mouse that I've used off-and-on for a couple years now. I've always been a fan of that form factor, which eases wrist pain and feels more natural to hold, but I've never been a tremendous fan of the Lift Mouse. The plastic tends to wear down over time, turning into a smooth and oily service that feels unpleasant to hold for very long. It's also not quite large enough for my hands, although in fairness to Logitech, they do point out it's for small-to-medium sized hands, and suggest their MX Vertical mouse for larger-handed people like me. I have tested the MX Vertical mouse in stores, but it feels even less pleasant to me than the Lift, despite a slightly larger size.

But the mouse I found, a JBuds Ergo Mouse, immediately felt comfortable and pleasant in my hand. It was the right size, and a slightly different angle that felt even more natural and comfortable to me. Plus, it doesn't feel like it has the same rubberized coating that tends to turn gross with the Logitech.

It was half the price of a Logitech Lift mouse, and the one I have is getting worn out anyway, so I decided to take a chance on it after reading a few threads online from Linux users to make sure that there weren't any major compatibility issues.

I'm very impressed with this mouse. It pairs easily (to multiple devices), wakes and connects quickly, and is pleasant to use. It has a DPI switcher, back and forward thumb buttons, and a customizable button on top.

As a Linux person, I assumed I'd never be able to use the button, but to my absolute delight it registers as a basic keypress (Super +D). I was able to go into the Keyboard Settings and assign a custom shortcut to execute `dbus-send --session --dest=org.gnome.Shell --type=method_call /org/gnome/Shell org.freedesktop.DBus.Properties.Set string:org.gnome.Shell string:OverviewActive variant:boolean:true`, which launches the overview in GNOME Shell. Now, with the press of a single button, I can move to a different window or find a new app to start.

Even if it were to be the same price as the Lift or Logitech MX Vertical I would _still_ prefer it over those others, but the fact that it retails at $39 makes it a no-brainer for me. If you're in the market for a new mouse, or if you've never tried using a vertical mouse before, you really can't go wrong with this one.
