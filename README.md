# My configuration and documentation on Sway window manager on Arch Linux

## Initial packages:
```
# pacman -S sway swaybg wofi waybar xorg-xwayland xorg-xhost
```

## Starting sway:
* Add following to ```$HOME/.zprofile```:
```
[ "$(tty)" = "/dev/tty1" ] && exec sway --unsupported-gpu
```

## GDM:
```
pacman -S gdm
```
```
systemctl enable gdm
```
Nvidia:
```
ln -s /dev/null /etc/udev/rules.d/61-gdm.rules
```
Add ```--unsupported-gpu``` to ```Exec``` line in ```/usr/share/wayland-sessions/sway.desktop```

## Qt apps:
* Install ```qt5ct```, ```kvantum```, ```breeze``` and ```breeze-icons```
* Choose a theme in Kvantum
* Apply ```kvantum-dark``` and choose an icon theme in Qt5ct
* Add ```QT_QPA_PLATFORMTHEME=qt5ct``` to ```/etc/environment```

## Gtk apps:
* Install ```gnome-tweaks``` and ```gnome-themes-extra```
* Choose Adwaita_Dark and a desired icon theme in ```gnome-tweaks```
```
gsettings set org.gnome.desktop.interface color-scheme 'prefer-dark'
```

## Clipboard
* Install ```copyq```

## Screenshots
* Install ```grim```, ```slurp``` and ```wl-clipboard```

## OBS Studio black preview fix
* Add ```nvidia-drm.modeset=1``` to kernel parameters

## Notifications
* Install ```swaync``` (AUR)

## Policy Kit GUI Authentication
* Install ```polkit-kde-agent```

## Set Dolphin as default file manager:
```
xdg-mime default org.kde.dolphin.desktop inode/directory
```

## Set Firefox as default browser:
```
xdg-settings set default-web-browser firefox.desktop
```

## Dolphin Alacritty
* Add following to ```$HOME/.config/kdeglobals```:
```
[General]
TerminalApplication=alacritty
```
