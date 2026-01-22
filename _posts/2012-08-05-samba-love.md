---
layout: post
title: "Samba love"
date: 2012-08-05
tags:
  - Microsoft
  - network
  - samba
  - sharing
  - smb
categories:
  - Computers
---

I'm going to do something today that I rarely do: give Microsoft some props.<!--more-->

Over the years it's arguable that they have screwed up just about everything they have put their hands on, but there is one project out there that they nailed off-the-bat: SMB.

SMB, or "Server Message Block" (which it has never been called in the history of forever, as it essentially has no meaning), is "an application-layer network protocol mainly used for providing shared access to files, printers,... and miscellaneous communications between nodes on a network. It also provides an authenticated inter-process communication mechanism."<a href="http://en.wikipedia.org/wiki/Server_Message_Block" target="_blank"> (From the SMB Wikipedia Article)</a>

In English, that means that it's a file sharing protocol that allows you to share files, printers, and other things- and lets users log in to access them. On the whole, that's not really a big deal; there are many protocols that give you similar functionality.

But here's the thing: <strong>it just works.</strong>

<strong>Samba</strong>, the free software SMB implementation, is<strong> the single-best way to share content on a local network.</strong> What's great about SMB is that everything can play well together: Windows, Mac, and Linux can all share on a local network together.

[caption id="attachment_1094" align="aligncenter" width="400"]<a href="http://nathandyer.wordpress.com/wp-content/uploads/2012/08/the-lion-king_l.jpg"><img class="size-full wp-image-1094" title="Simba" src="http://nathandyer.wordpress.com/wp-content/uploads/2012/08/the-lion-king_l.jpg" alt="" width="400" height="300" /></a> Samba, not Simba[/caption]

But not only that, there's no tricky configuration. Any idiot can share a printer or add a shared folder or drive. Two-clicks and you're done. It works out of the box.

So, good on you, Microsoft. At least you did one thing right.