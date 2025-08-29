---
layout: post
title: The Masochist's Save File Dialog
summary: This thing is the bane of my existence
---

I spend a substantial amount of time in my text editor, which happens to be the default text editor for the GNOME desktop environment (`gnome-text-editor`). And everyday, I find myself having to contend with what has become the bane of my existence: its ambiguously designed save dialog.

At first, this looks like a perfectly cromulent file save dialog that might appear after pressing the close button in an attempt to exit the program. When you have just a single document open, the dialog _mostly_ makes sense. It presents you with an option to either save or discard:

![The file save dialog with a single checked item]({{ site.url }}/img/single_checked.jpg)

The problem here is that it also includes a checkbox, which in a single-file scenario, has absolutely no effect on the function of the buttons. Whether or not the box is checked, Discard exits without saving the changes, and the Save button writes the changes to disk and then exits. I guess that's consistent with what the buttons say they will do, but there's a part of me that thinks clicking Save shouldn't actually Save when the document is unchecked. 

![The file save dialog with a single unchecked item]({{ site.url }}/img/single_unchecked.jpg)

When there's only a single document, and the box is unchecked, should the Save button not disappear entirely? But no matter, I can work with this.

That behavior does beg the question, though, what happens when you have multiple documents open within tabs in the same window? This is when chaos ensues. If you have multiple documents open, you are presented with options to Discard All or Save. When all the checkboxes are checked, it's mostly straightforward: clicking Save will write all changes to disk from all the open documents, and clicking Discard All will get rid of them all.

![The file save dialog with multiple checked items]({{ site.url }}/img/multiple_uniform.jpg)

But if you only have some checked and click Save? Only the ones checked get written to disk. That makes sense too, I suppose. And if you have some checked and click Discard All? The checkbox doesn't matter and they all get discarded. Again, I guess that makes sense.

![The file save dialog with a mix of checked and unchecked items]({{ site.url }}/img/multiple_mixed.jpg)

What really goes into broken/scary territory is when you have text in a tab that isn't part of an existing document, and you check its box to save alongside documents that do already exist. Do you get a dialog to choose a path and name? No, at least not in my experience. Instead, it saves the documents it knows about, exists, and completely discards the text you've written in the tab that isn't part of a pre-existing file. Yikes!

The bad part is, I'm not sure which of these issues are bugs versus UX papercuts. Part of me thinks maybe _my brain_ is the problem. In any case, these dialogs are starting to appear not just in the Text Editor app, but in other apps as well. I do think they're a visual improvement over the old styles, but a little UX polish might go a long way.
