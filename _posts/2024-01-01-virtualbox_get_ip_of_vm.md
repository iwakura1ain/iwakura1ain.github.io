
# Table of Contents

1.  [virtualbox get ip of vm](#orga2f88e4)


<a id="orga2f88e4"></a>

# virtualbox get ip of vm

    either one of these two
    requires virtualbox addon package

    vboxmanage guestproperty get [VM-NAME] "/VirtualBox/GuestInfo/Net/0/V4/IP"
    vboxmanage guestproperty get [VM-NAME] "/VirtualBox/GuestInfo/Net/1/V4/IP"

