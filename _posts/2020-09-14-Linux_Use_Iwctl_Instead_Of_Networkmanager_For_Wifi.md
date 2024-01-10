---
title: "Linux Use Iwctl Instead Of Networkmanager For Wifi"
date: 2020-09-14 15:20:05 +0900
layout: post
categories: 
tags: 
---

-   linux use iwctl instead of networkmanager for wifi

    stop/disable NetworkManager.service
    start/enable iwd.service

{% highlight bash %}
sudo iwctl
station wlan0 scan # scan networks
station wlan0 get-networks # get scan list
station wlan0 connect [SSID] [PW]
{% endhighlight %}
