---
layout: post
title: I Don't Care About Browser Engines
summary: I know I should. But I don't.
---

I'll be honest: I don't really care about browser engines.

I know that's something that I _should_ care about as a person who has taken a number of principled stands over the years, especially in regards to free software and the future of technology.

The argument goes, I suppose, that you don't want there to just be a single browser engine. It's really about power here. If you have a browser engine that is primarily developed by, or at least funded by, a single organization, then that organization gets to make all the decisions and call all the shots. And because of the nature of organizations with power, they would wield that power in anti-competitive ways that would give them the edge to provide the best user experience at the detriment of others, allowing them to steal marketshare.

But from the way I see it, we are not anywhere close to that point yet.

I have heard the arguments time and time again that there are realistically two browsers: Firefox, and Chrome + dozens of skinned version of Chrome. Vivaldi, Microsoft Edge, Brave, and pretty much every other browser you can think of (short of forks of Firefox) are built on top of Chromium's libraries and use Blink as a rendering engine. You're made to believe it's a Blink vs. Gecko world out there, and you're just living in it.

I think that's a false dichotomy.

For one, I think that fails to consider the larger WebKit ecosystem. Google may have taken WebKit and forked it into Blink, but WebKit was originally created at Apple (although I believe it was based on KHTML, so its roots are strangely enough grounded in KDE), and is one of the few examples of Apple actually embracing open source and contributing to it in a meaningful way. Apple does not have full control over WebKit, and plenty of other browsers use it. Most notably for my interests, you have WebKitGTK which powers GNOME Web browser (aka Epiphany), and can also be bundled into apps such as email clients and RSS feed readers to render HTML. Google might be the dominant player when it comes to Blink, but it does not dominate WebKit. Arguably Apple dominates WebKit, but even there I see plenty of contributions for lots of other organizations.

That's not to mention the work that's underway for a next generation of standalone web engines. The most interesting to me is Servo, the engine written in Rust from the ground up and designed in a way that is meant to be easily embedable from the get-go. As it stands, I happen to like the inclusive way that they tend to operate their community. There's also the Ladybird browser with its new web engine currently in development. I'm cautiously optimistic there, although I'm a bit more worried that it operates and appeals more to the liberarian/alt-right-ish side of the FOSS crowd.

To be clear, I don't think that Gecko is such an incredibly dominant player that having it disappear tomorrow would be a disastrous situation in which you would only have one engine that is dictated by a big tech monopolist organization. 

And with that in mind, I really don't think it's worth clinging to Firefox as the end-all-be-all savior of the open web. For the time being, from a purely pragmatic perspective, I find that Firefox is still the most stable browser and the best integration with my GNOME desktop environment (with GNOME Web closing that gap quickly). It also seems to work well in KDE and Pantheon, from what little I've used it there in recent years.

When that stops being the case, or when Mozilla finish their inevitable slide into a full-on AI slop factory, I will feel no guilt. A mild twinge of disappointment, perhaps, but only for what could have been.

And this is coming from a guy that used to have an "I donated to Mozilla!" certificate hanging on the wall in his teenage bedroom.
