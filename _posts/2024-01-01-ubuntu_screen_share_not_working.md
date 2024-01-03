
# Table of Contents

1.  [ubuntu screen share not working](#org525be79)


<a id="org525be79"></a>

# ubuntu screen share not working

    use xorg, not wayland

    echo $XDG_SESSION_TYPE
    sudo nano /etc/gdm3/custom.conf

    WaylandEnable=false

