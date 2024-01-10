---
title: "Ubuntu Screen Share Not Working"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   ubuntu screen share not working

    use xorg, not wayland

{% highlight bash %}
echo $XDG_SESSION_TYPE
sudo nano /etc/gdm3/custom.conf
{% endhighlight %}

{% highlight nil %}
WaylandEnable=false
{% endhighlight %}
