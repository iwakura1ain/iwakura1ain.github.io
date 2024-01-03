---
layout: post #jekyll layout
title: "Virtualbox Get Ip Of Vm" #title 
date:   2020-09-14 15:20:05 +0900                 
---

-   virtualbox get ip of vm

    either one of these two
    requires virtualbox addon package

    vboxmanage guestproperty get [VM-NAME] "/VirtualBox/GuestInfo/Net/0/V4/IP"
    vboxmanage guestproperty get [VM-NAME] "/VirtualBox/GuestInfo/Net/1/V4/IP"

