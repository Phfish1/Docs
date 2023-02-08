### Sound

Pulseaudio [Arch](https://wiki.archlinux.org/title/PulseAudio#Installation)
```
$ pacman -S pulseaudio pulseaudio-bluetooth
```

GUI / Front end
```
$ pacman -S pavucontrol
```

### Bluetooth

BlueZ for Bluetooth
```
$ pacman -S bluez bluez-utils 
```
bluez-utils (BluetoothCLI) | Blueman (GUI) | Bluedevil (KDE)

Enable
```
$ systemctl enable bluetooth
```

### File manager

**Dolphin** or Thunar
```
$ pacman -S dolphin
```

Image viewer | `feh` = (mininal) | **nomacs**
```
$ pacman -S nomacs
```

