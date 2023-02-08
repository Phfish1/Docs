### Xorg

Install
```
$ pacman -S xorg-server xorg-apps xorg-xinit xterm
```

Find VGA device 
```
$ lspci | grep -e VGA
```

Install VGA Driver.
```
$ sudo pacman -S nvidia
```

### LightDM 

**Display Manager** that works on all Desktops enviroments

install | or `lightdm lightdm-gtk-greeter lightdm-gtk-greeter-settings`
```
$ pacman -S lightdm lightdm-webkit2-greeter
```

**Edit*** `/etc/lightdm/lightdm.conf`:
```
greeter-session=lightdm-webkit2-greeter
```

enable
```
$ systemctl enable lightdm
```

Test: `$ lightdm --test-mode --debug`

**Theme**
Install
```
# yay -S lightdm-webkit-theme-aether
```

Edit `/etc/lightdm/lightdm-webkit2-greeter.conf`
```
webkit_theme = aether
```
Might need full name: lightdm-webkit-theme-aether

### DESKTOP ENVIROMENT

Update First
```
$ pacman -Syu
```

[[KDE Plasma]]

[[Cinnamon]]

### Display

Use `$ xrandr | grep connected` and
```
$ xrandr --output DP-4 --primary --left-of DP-0
```

Edit / Create `/etc/X11/xorg.conf.d/10-monitor.conf`
``` conf
Section "Monitor"
    Identifier  "DP-4"
    Option      "Primary" "true"
EndSection

Section "Monitor"
    Identifier  "DP-0"
    Option      "RightOf" "DP-4"
EndSection
```

Might also need to change Desktop enivroment ( display settings )