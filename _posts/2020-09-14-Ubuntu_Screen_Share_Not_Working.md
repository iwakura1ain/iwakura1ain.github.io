---
layout: post #jekyll layout
title: "Ubuntu Screen Share Not Working" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   ubuntu screen share not working

    use xorg, not wayland

    echo $XDG_SESSION_TYPE
    sudo nano /etc/gdm3/custom.conf

    WaylandEnable=false

