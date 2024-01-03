
# Table of Contents

1.  [linux use iwctl instead of networkmanager for wifi](#orga48f626)


<a id="orga48f626"></a>

# linux use iwctl instead of networkmanager for wifi

    stop/disable NetworkManager.service
    start/enable iwd.service

    sudo iwctl
    station wlan0 scan # scan networks
    station wlan0 get-networks # get scan list
    station wlan0 connect [SSID] [PW]

