Based on: https://www.arcolinuxd.com/6-the-actual-installation-of-arch-linux-phase-2

### Users

Edit UnComment **visudo** file | `pacman -S vi || export EDITOR=vim;
```
%sudo ALL=(ALL:ALL) ALL
```

Add group **sudo**
```
# groupadd sudo
```

Add main user
```
# useradd -mG sudo -s /bin/bash phfish
```

Password
```
# passwd phfish
```

### Multilib

Enable Multilib: `vim /etc/pacman.conf`
```
[multilib]
include = /etc/pacman.d/mirrorlist
```

```
$ pacman -Syu
```

Install **yay**

```
$ git clone https://aur.archlinux.org/yay.git
$ cd yay
$ makepkg -si
```

### Console

Configure default FONT: `/usr/share/kbd/consolefonts`
```
$ setfont ter-v22n
```

Edit `/etc/vconsole.conf`
```
FONT=ter-v22n
```

See **[[Terminal#Powerline| Powerline]]** configuration

>If not changing. edit **mkinitcpio** `/etc/mkinitcpio.conf` | `$ mkinitcpio -P`
>See [ArchFonts](https://wiki.archlinux.org/title/Linux_console#Persistent_configuration) [ArchMkinitcpio](https://wiki.archlinux.org/title/Kernel_mode_setting#Early_KMS_start)
