# My configuration and documentation on Sway window manager on Arch Linux

## Initial packages:
```
# pacman -S sway swaybg wofi
```

## Starting sway:
* Add following to ```$HOME/.zprofile```:
```
[ "$(tty)" = "/dev/tty1" ] && exec sway --unsupported-gpu
```

## Qt apps:
* Install ```qt5ct```, ```kvantum```, ```breeze``` and ```breeze-icons```
* Choose a theme in Kvantum
* Apply ```kvantum-dark``` and choose an icon theme in Qt5ct
* Add ```QT_QPA_PLATFORMTHEME=qt5ct``` to ```/etc/environment```

## Gtk apps:
* Install ```gnome-tweaks``` and ```gnome-themes-extra```
* Choose Adwaita_Dark and a desired icon theme in ```gnome-tweaks```

## Some apps being unable to open a display
* Install ```xorg-xwayland``` and ```xorg-xhost```
* Run:
```
xhost +local:
```

## Clipboard
* Install ```copyq```

## Screenshots
* Install ```grim```, ```slurp``` and ```wl-clipboard```

## OBS Studio black preview fix
* Use ```nvidia-dkms```
* Add ```nvidia-drm.modeset=1``` to kernel parameters

## Notifications
* Install ```swaync``` (AUR)

## Policy Kit GUI Authentication
* Install ```polkit-kde-agent```
---
### Additional stuff
Photo viewer: ```imv```
