---
layout: post
title: "A Linux User's Review of Doxie Go"
date: 2014-03-13
categories:
  - Uncategorized
---

Last year, in my mission to go paperless and digitize all of my photos and documents, I began searching for the perfect scanner. It wasn’t long until I came across several recommendations for Doxie.

<a href="http://nathandyer.wordpress.com/wp-content/uploads/2014/03/2014-03-13-18-05-59.jpg"><img class="aligncenter size-full wp-image-1453" alt="2014-03-13 18.05.59" src="http://nathandyer.wordpress.com/wp-content/uploads/2014/03/2014-03-13-18-05-59.jpg" width="1008" height="258" /></a>

Doxie is a brand of digital scanners that aims to be really simple to use. It comes coupled with software that makes importing and editing scans supremely easy, and provides integration with cloud services like Dropbox and Evernote. It seemed that all the reviews were overwhelmingly positive, but I couldn't find any from Linux users. Linux isn't officially supported, but as it turns out it <strong>you can use Doxie with Linux quite painlessly.</strong>
<h3>Hardware</h3>
After comparing the different models I settled on the Doxie Go. Doxie Go is a portable scanner, meaning that you can take it anywhere and scan at any time. It’s so compact and lightweight that you can throw it in a backpack. The other main advantage to that model over the cheaper ones is that it has a high DPI setting that comes in very handy for archiving photos in the best possible quality (see example below).
<p style="text-align:center;"><a href="http://nathandyer.wordpress.com/wp-content/uploads/2014/03/doxie-0011.jpg"><img class="aligncenter  wp-image-1461" alt="Baby Me" src="http://nathandyer.wordpress.com/wp-content/uploads/2014/03/doxie-0011.jpg?w=819" width="393" height="491" /></a></p>
It includes a built-in battery that, as far as my usage suggests, seems to last for ~100 scans. The battery life is good, but it takes longer to charge than I expected. I've noticed it can take several hours to charge, depending how low your battery is.

The Doxie Go now comes with an AC adapter, and that makes all the difference. My first one did not come with the power adapter, so extended scanning sessions were frustrating. I could only make about a hundred scans, and then would have to wait for the battery to recharge completely. Now, I just plug it into the wall and scan as much as I’d like. The experience couldn’t be better.

It comes with a cleaning tool and a photo sheet that makes scanning photos painless. The hardware is very high-quality and doesn't feel cheap in the slightest. It is prone to cosmetic scratches, but it shouldn't be too much of a problem if you try to be gentle with it.
<h3>Use a SD Card</h3>
I’ve had the scanner for about nine months now, and in that time I’ve discovered that there’s a right way and a wrong way to use it. A lot of it is because I’m a Linux user, but in many ways this applies to everyone across all platforms.

I cannot recommend purchasing an SD card enough. For the first few months I used only the internal memory built-in to the scanner, but there were some issues with that. For one thing, I noticed at times after many scans images started getting corrupted or disappearing entirely from the internal storage. It's also worth noting that after about six months my internal storage got corrupted and it completely killed my Doxie, although I'm not sure if that was a defect with the device or if Linux did something nasty to the internal memory by accident. Regardless, the safe way is to always use a SD card.
<h3>Workflow with Ubuntu-based Systems</h3>
Sadly, the Doxie software doesn’t work with Linux. For Mac and Windows it provides an easy way to import scans, edit them, save them in many different formats, and auto-upload to Dropbox and Evernote. The official software might not be available for Linux, but you can still do almost all of that using native apps.

After inserting the SD card (or connecting the Doxie directly, if you choose to disregard my above suggestion) you can navigate directly to the storage device in your file browser. Inside you’ll find all the scans as .jpg files. At this point you can either manipulate the files directly, or copy them elsewhere and keep the original copies safe in case you need to access them again.

Editing scanned photos is very easy. Using your preferred photo editor of choice (I’ve found that Shotwell fits almost all of my needs for photo editing), you can open the scans just as you would any other photo. If you have used the photo sleeve it’s likely that you may not have to make many adjustments, except perhaps some additional cropping.

As for documents, it’s actually easier than you might think to create PDFs from your scans. Edit the .jpg scans of the documents to make sure they are cropped and orientated the way you would like. Additionally, you can use a tool like GIMP if you need to boost the contrast or brightness (although I’ve found that most documents are fine just as they are scanned). Then, use a command-line tool called convert to create PDF versions.

To install convert, either search the Software Center for it or install via terminal:
<pre>sudo apt-get install convert</pre>
After that, just call convert in the terminal using the input file (you can input mutiple files to put them together into a single PDF) and tell it an output name. For example:
<pre>convert ScannedDoc1.jpg ScannedDoc2.jpg CombinedDoc.pdf</pre>
<h3>Doxie Support</h3>
As I mentioned before, at one point the internal memory on the scanner became corrupted and required a replacement. Doxie Support was absolutely outstanding. With a couple tweets they sent me a brand new scanner, as well as a pre-paid shipping label to send my dead one back.
<h3>Overall Feelings</h3>
I absolutely love my Doxie Go. Scanners have a bad reputation for being problematic, but Doxie is a breeze to use. It’s very well-made and, if having digital scans of your photos and documents is important to you, it’s worth every penny.