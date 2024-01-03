---
layout: post #jekyll layout
title: "Linux Use Iwctl Instead Of Networkmanager For Wifi" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   linux use iwctl instead of networkmanager for wifi

    stop/disable NetworkManager.service
    start/enable iwd.service

    sudo iwctl
    station wlan0 scan # scan networks
    station wlan0 get-networks # get scan list
    station wlan0 connect [SSID] [PW]

