!1. swap capslock and ctrl_L keys, Create file .xmodmap_capslock in home with following content
```
remove Lock = Caps_Lock
remove Control = Control_L
keysym Control_L = Caps_Lock
keysym Caps_Lock = Control_L
add Lock = Caps_Lock
add Control = Control_L 
```
!2. To make the swap effective after restart create a xmodmapp_capslock.desktop file in folder ~/.config/autostart with following content
```
[Desktop Entry]
Name[en_US]=Xmodmap
Comment[en_US]=xmodmap ~/.xmodmap
Exec=/usr/bin/xmodmap .xmodmap
Icon=application-default-icon
X-GNOME-Autostart-enabled=true
Type=Application
```
!3. To get default functionality run following command and delete above two files.
```
setxkbmap -option
```
