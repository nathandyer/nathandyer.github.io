---
layout: post
title: The Current GNOME App Landscape, and the Two Apps I Wish Existed
summary: It's the best time in history to be a GNOME user. There are only two apps I feel that are missing.
date: 2026-02-19 20:00:00 -0500
---

I know the popular thing in modern times is to dislike standalone applications, and when it comes to apps on platforms like iOS and Android, I generally agree. More often than not, apps are black boxes that spy on you, rip you off, and in some cases, endanger your livelihood. Not to mention that they often use mechanisms under the hood to prevent you modifying or studying their behavior, and if you try to bypass those protections you can find yourself in violation of section 1201 of the DMCA and facing enormous fines and/or jail time.

But while this is true, using free and open source applications can be a really pleasant experience, and they will often provide you with a better experience than what you can find using a modern web app. I still love apps, especially those written using GTK and Adwaita, and made available via Flatpak through Flathub or other Flatpak repositories.

I'm genuinely amazed at the quality and variety of apps that I have available on my laptop, which currently (and for the past decade or so) is running Fedora with stock GNOME. We're in a better state than I could have dreamed, and I get more enjoyment and utility out of my computer every single day because of these apps made by (mostly) independent developers all across the world and from all walks of life.

I want to be encouraging to developers, and point out that anyone with the technical know-how can get involved either with an existing project or, with a little determination and willingness to learn, start a project of their own. 

At the same time, I think there is an underlying truth about the universe: there are only so many things that humans need or want to do, and for the most part, there are already ways of doing them quickly and easily on the computer.

There aren't many gaps in my computing where I want to be able to achieve a task, but don't currently have the means to do so.

From my perspective, there are only two apps that don't currently exist as GNOME apps that I would love to see: a package tracking app, and an Adwaita email client.

On the package tracking front, I occasionally buy things online, and would really like a package tracker that lists all the different shipments I have in progress and shows me the latest tracking information for each of them, along with estimated delivery dates, and then sends me notifications whenever there is a new update about a package's whereabouts. On iOS, I use the app Parcels, and it's excellent (although I find that notifications don't always trigger like they should).

A while back I teased that I had been working on such an app, and you can see a screenshot of what I have below:

![A screenshot of a work-in-progress tracking app, with two sample deliveries displayed in the middle featuring estimated delivery dates, a description, and the carrier name]({{ site.url }}/img/tracker_screenshot.png)

All of the browsing/adding/removing/sorting functionality is in place and functional, but I haven't been able to finish the rest of the app yet, because I don't have a way of reliably pulling information from the various shipping providers. Proprietary apps have the advantage of being able to include unique API keys for all the various services, but being an open source app, I've not yet found a reliable way of storing said keys in a way that's inaccessible to the user (and if I did, it wouldn't really be open source). That means a user would have to individually sign up for developer accounts and generate API keys with each provider they want to use for tracking. What a horrible user experience! I've also tried various methods of scraping, but this would be extremely brittle because any new anti-scraping measurements or changes in how information is delivered on the part of the vendors would result in breakages within the app.

The second app that doesn't yet exist is an Adwaita-based email client. I used to love Geary back in the GNOME 3 days, but as Yorba disbanded and development fell back to the community it started receiving fewer updates, and began to break in various places. I think development is still technically ongoing (and now it is maintained by GNOME itself to varying degrees), but it hasn't seen a ton of modernization or improvement over the past decade or so.

I'm excited about a new potential app called [Envelope](https://gitlab.gnome.org/felinira/envelope), but so far there haven't been any previews, nor activity in the repo for the past four months as far as I'm aware, so it may be a while yet before this is a viable option.

Still, how incredible is it that in the modern Linux ecosystem, I'm able to achieve almost everything I want to do with the apps that exist! There are thousands of apps in the Flathub "store", with almost all of them receiving regular updates directly from the developers. It is the best time in history to be a Linux user, and I'm continuously impressed by the work that the Flatpak and Flathub communities have done (and are doing) to make this dream a reality.

