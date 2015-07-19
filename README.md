# LightDM Webkit Arch Theme
This is a LightDM webkit greeter theme for Archlinux. To be used as a single user with a single session choice, no session choice on login screen. Based on https://github.com/shosca/lightdm-webkit-archlinux-theme.

## Installation Instructions
You will need lightdm as your login manager and the `lightdm-webkit2-greeter` from AUR. You need to make the webkit greeter the default greeter. This is done by editing the lightdm configuration under:

    /etc/lightdm/lightdm.conf

Changing the `greeter-session` value to lightdm-webkit-greeter. lightdm.conf should have:

    [SeatDefaults]
    greeter-session=lightdm-webkit-greeter
    allow-guest=false

Set `user-session` in `lightdm.conf` to the session you wich to use. For Awesome VM this would be `awesome`.

### Install the actual theme
Get it from AUR `lightdm-webkit-archsingle-theme`.

Or copy the files of this repository into the following location:

    /usr/share/lightdm-webkit/themes/archsingle

Finally, change the /etc/lightdm/lightdm-webkit-greeter.conf file to contain the following line:

    webkit-theme=archsingle

Now you can reboot and enjoy the new theme.

## Background
The included background come from https://unsplash.com/.

You may change the background by swapping the `background.jpg` in the theme directory, ``/usr/share/lightdm-webkit/themes/archsingle`.
