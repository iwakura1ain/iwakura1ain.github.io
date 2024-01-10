---
title: "Linux Yay Install With Modified Build Files"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   linux yay install with modified build files

    build checks failed while installing aur/lib32-libgit2 -> so comment out checks in build file

{% highlight bash %}
yay --editmenu -S [PACKAGE]
{% endhighlight %}
