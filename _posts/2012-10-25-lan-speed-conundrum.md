---
layout: post
title: "LAN Speed Conundrum"
date: 2012-10-25
categories:
  - Uncategorized
---

Dear people who understand networking better than me: I need a favor.

I have been obsessed with getting my local network here at my house running top notch the past few months. I'll share more of my setup at a later date, but I have a couple issues that are really stumping me.

I have an ASUS RT-N12 router running DD-WRT. After some reading up and studying I am finally able to take advantage of my 802.11 N connection. Although DD-WRT doesn't support the 5GHz radio (which means no 300Mb/s for me),<strong> I am able to consistently establish a 150Mb connection between my devices now. </strong>

<strong>I have a Raspberry Pi connected to a 1TB HDD (SATA dock &gt; USB) that, among other fun things, primarily shares that disk out via SMB</strong>. I have all my DVD and Blu-ray rips on there so I can stream them over the network, and we also use it for general network storage. <strong>The Raspberry Pi is connected to my router via standard Cat5e cable.</strong>

Now to the essence of this post: I have noticed that reading and writing from that HDD has been slower than it should. I cannot, to save my life, figure out it out.

<a href="http://nathandyer.wordpress.com/wp-content/uploads/2012/10/screenshot-from-2012-10-25-091030.png"><img class="aligncenter size-full wp-image-1218" title="Screenshot from 2012-10-25 09:10:30" alt="" src="http://nathandyer.wordpress.com/wp-content/uploads/2012/10/screenshot-from-2012-10-25-091030.png" height="250" width="450" /></a>

<a href="http://nathandyer.wordpress.com/wp-content/uploads/2012/10/screenshot-from-2012-10-25-084031.png"><img class="aligncenter size-large wp-image-1213" title="Screenshot from 2012-10-25 08:40:31" alt="" src="http://nathandyer.wordpress.com/wp-content/uploads/2012/10/screenshot-from-2012-10-25-084031.png?w=1024" height="575" width="1024" /></a>My two big questions are as follows:

<strong>1) Why is the data transfer speed not consistent? Why are there so many ups and downs in that graph? Is this normal?</strong>

<strong>2) Why is the speed so low? On a 150Mb connection, why am I only getting at best ~20Mb/s? (Transfer speed on the copy dialogue shows 1.7MB/sec. 150Mbps/8=18.75MBps, so shouldn't I get 15+ MB/sec? )</strong>