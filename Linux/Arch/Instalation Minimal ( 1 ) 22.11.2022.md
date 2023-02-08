Use: **UEFI** -> EFI_Boot_Loader
**Not: BIOS** -> MDR 

### Basic

Keyboard layout
```
# loadkeys no-latin1
```

Check if UEFI.
```
# ls /sys/firmware/efi/efivars
```

Connect to internet
```
# iwctl
[iwctl]# device list
[iwctl]# station wlan0 scan
[iwctl]# station wlan0 get-networks
[iwctl]# station wlan0 connect SSID
```

```
# ip link && ping archlinux.org
```

TimeAndDate ( **USE UTC** ) for hardware clock
```
# timedatectl set-ntp True
```

```
# timedatectl status
```

### Partinioning ( Fdisk )
 
Partition1 | BOOT = 300M | 1 // EFI System
Partition2 | ROOT = Rest | 23 // Linux root x86-64
swap = none

List disks
```
# fdisk -l
```

Choose disk
```
# fdisk /dev/sda
```

Partition

p = print partition
i = info

**g** = new **GPT** partition table
d = delete partition
n = new partition

### Format / Mount

For root / main partition
```
# mkfs.ext4 /dev/sda2
```

For boot partition
```
# mkfs.fat -F 32 /dev/sda1
```

Mounting ROOT Partition
```
# mount /dev/sda2 /mnt
```

Mount BOOT || `mkdir /boot/efi`
```
# mount /dev/sda1 /mnt/boot/efi
```

### Installing
mirrorlist `/etc/pacman.d/mirrorlist` | `# reflector`

```
# pacstrap /mnt base base-devel linux linux-firmware vim
```

### Chroot

Fstab to mount disks at startup
```
# genfstab -U /mnt >> /mnt/etc/fstab
```

Chroot
```
# arch-chroot /mnt
```

### Time / Locale

TimeZone
```
# ln -sf /usr/share/zoneinfo/Europe/Oslo /etc/localtime
```

Hardware Clock
```
# hwclock --systohc
```

Set Locale
`vim /etc/locale.gen` **Uncomment**:
```
en_DK.UTF-8 UTF-8
en_DK ISO-8859-1
```

and run
```
# locale-gen
```

Lang variable | `vim /etc/locale.conf`:
```
LANG=en_US.UTF-8
```

Keyboard Layout | `vim /etc/vconsole.conf`
```
KEYMAP=no-latin1
```

### Network

Hostname | `vim /etc/hostname`
```
PHAM
```

**Downloads**
```
# pacman -S networkmanager
```

Extra
```
# pacman -S man-db man-pages tldr bash-completion
```

Enable NetworkManager

```
# systemctl enable NetworkManager
```

### GRUB

Download
```
# pacman -S grub efibootmgr
```

Install
```
# grub-install --target=x86_64-efi --efi-directory=/boot/efi
```

make config file | Only edit `/etc/default/grub` | `GRUB_GFXMODE=1920x1080x32`
```
# grub-mkconifg -o /boot/grub/grub.cfg
```

### Last

Initramfs | mkinitcpio 
```
# mkinitcpio -P
```

Password
```
# passwd
```

EXITING
```
# exit
```

root@archiso
```
# umount -R /mnt
```

```
# reboot
```