---
layout: post
title: Markdown and HTML
---

Jekyll supports the use of [Markdown](http://daringfireball.net/projects/markdown/syntax) with inline HTML tags which makes it easier to quickly write posts with Jekyll, without having to worry too much about text formatting. A sample of the formatting follows.

Tables have also been extended from Markdown:

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

Here's an example of an image, which is included using Markdown:

![Geometric pattern with fading gradient](/img/sample_feature_img_2.png)

Highlighting for code in Jekyll is done using Pygments or Rouge. This theme makes use of Pygments by default.

{% highlight css %}
nav a:hover {
  color: rgba(0,0,0,.72);
}
nav a.current {
  color: rgba(0, 0, 0, .72)
}
.subtitle {
  margin: 30px 0;
}
{% endhighlight %}

You can also add line numbers by setting `linenos`. Like in this example:

{% highlight bash linenos %}
#!/bin/bash

###### CONFIG
ACCEPTED_HOSTS="/root/.hag_accepted.conf"
BE_VERBOSE=false

if [ "$UID" -ne 0 ]
then
 echo "Superuser rights required"
 exit 2
fi

genApacheConf(){
 echo -e "# Host ${HOME_DIR}$1/$2 :"
}
{% endhighlight %}

Note that when you try to copy this code block the line numbers will be copied too.