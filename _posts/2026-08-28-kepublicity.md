---
layout: post
title: Why I Made 'Kepublicity'
summary: Part scratching my own itch, part practicing good FOSS hygiene
date: 2026-08-28 15:30:00 -0400
---

If you follow me on Mastodon, you might have noticed that I launched a new app a few weeks ago, which is [available now on Flathub](https://flathub.org/en/apps/me.nathandyer.Kepublicity). The name is Kepublicity, and it's a GNOME app for people who like to send book files from their computer to a Kobo ereader.

It serves two main functions:

1. Converting standard .epub files to Kobo-formatted .kepub files, and
2. Sending converted files to a connected Kobo device

Under the hood, it uses [kepubify](https://github.com/pgaskin/kepubify) to do the conversions.

![An example of a batch conversion within Kepublicity, with four files set to be copied directly to a Kobo device](https://codeberg.org/nathandyer/Kepublicity/raw/branch/main/screenshots/book-list.png)

## Kepublicity as a tool

I was inspired to write it because I was honestly tired of having to go through Calibre every time I wanted to convert a book. While Calibre is an impressive piece of software that works incredibly well, the install size approaches 1GB, it maintains a separate library, includes a handful of other apps/utilties, and is just completely overkill for the workflow that I use.

While looking for alternative options I found myself using web-based converters, then command line-based converters, and would ultimately end up mounting my Kobo and copying the converted files through a file browser. I longed for a simple utility that would do the entire workflow from start to finish, with little effort. Just open it, drag-and-drop a load of files, hit a button, and watch as they all convert and then get sent to the Kobo.

So that's what I built!

When I first launched the app, the main question I got was "why is it necessary to convert book formats, when Kobo supports epubs?" It's a fair question, especially for folks outside of the Kobo ecosystem, but there are actually several important reasons. The main reason is that Kobos actually have two different book renderers built-in. [epubs open in an outdated, slow Adobe-created renderer (RMSDK), while kepubs open in a more modern WebKit-based renderer.](https://andreklein.net/your-epub-is-fine-kobo-disagrees-blame-adobe/) Kepub books load faster, turn pages faster, support zooming in images, give you pop-up footnote links, provide time estimate measurements, work better with custom font faces and sizes, and are just generally the way to go on Kobo devices.

I'm not suggesting that you take a perfectly good epub file and forever toss it aside. The workflow I use is to keep a local library on my computer of my epub files, then convert on-the-fly as I need them, and store only the kepub versions on my Kobo.


## Kepublicity as an engineering project

There's another reason why I wrote Kepublicity: as an engineering challenge to myself, to try and reflect the ways I have grown as a developer.

In another life, when I created the Vocal podcast app as a college sophomore, I was completely new to software development, Vala, GTK, version control (remember Bazaar?), localization, and free software maintenance in general. I learned more and more about the field of software development and what it takes to be an effective open source maintainer, but I never really had the chance to showcase everything I had learned before I had to end the other projects I was working on. I never properly maintained Vocal (or any app) in a way that I was proud of.

So now, all these years later, what would it look like if I were to create a project using everything I've learned from a decade of software development, and after years of being a professional maintainer through my work on SecureDrop for Freedom of the Press Foundation?

In short, it looks like this: [https://codeberg.org/nathandyer/Kepublicity](https://codeberg.org/nathandyer/Kepublicity)

Within the repo, I hope technical users and developers will notice:
* A clean git history
* Small, self-contained commits
* Useful commit messages that roughly adhere to the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) format
* Proper [semantic versioning](https://semver.org/)
* An up-to-date changelog
* Releases with an accurate list of changes since the previous version

I don't yet have the localization story figured out, but within the next couple releases you should expect all the strings to be translatable, and then regular releases with new translations added as they roll in. Stay tuned.

The truth is that with the ever-expanding use of LLMs, I sometimes feel a measure of despair about the state of the software industry, and especially the FOSS environment as a whole. Sometimes it's nice to remind yourself that software can (should?) be a craft, with humans at the core. And I hope to also convince myself that I've improved in both expertise and skill since the first code I released all those many years ago. Of course, my bio still says "not a great developer, but I dabble," and I don't expect I'll be removing that line any time soon. There's always so much more to learn.

## Download and feedback

If you have a Kobo and you're using Linux, I really hope you'll take Kepublicity for a spin! It's available to download from Flathub here: [https://flathub.org/en/apps/me.nathandyer.Kepublicity](https://flathub.org/en/apps/me.nathandyer.Kepublicity)

If you have a feature request, run into an issue, or can think of a way to improve, I would really appreciate an issue report: [https://codeberg.org/nathandyer/Kepublicity/issues](https://codeberg.org/nathandyer/Kepublicity/issues)

Or if you want to share any feedback at all, you can contact me on Matrix, [Signal](https://signal.me/#eu/DnT1tyWhAif7gcoi0hzVc97Q1y2HXrqRJ5PbgRVukB7ES57CiFFIwJwmSWOF3poj), [Mastodon](https://hachyderm.io/@nathandyer), or [email](mailto:nathandyer@fastmail.com). I would really love to hear from you!

I hope you are able to get lots of use out of it!
