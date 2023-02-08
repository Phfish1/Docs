### Finding Drives

```
$ lsblk
```

### Partitioning ->

```
$ fdisk -l
```

```
$ fdisk /dev/sda
```

#### Formating ->

```
$ mkfs[.[ext4](Formating)] '/dev/sda1'
```

```
$ mkfs -t vfat -F 32 -n 'name' /dev/sdb1 `(--type), (FAT 32), (--name) `
```

For more info see [[Disk Managment#Formating Info|Formating info]]

### Mounting ->

```
$ mount /dev/sdb1 /media/usb
```

```
$ mount /dev/sda2 /mnt/drive1
```

```
$ mount | grep sdb `cheks if mounted`
```

```
$ unmount -l /dev/sdb `(--Lazy) #Forces even if bussy#`
```

**Auto mounting:** `mounts at startup`

```
$ vim /etc/fstab
```

**END of file:**
/dev/sdb    /mnt/sdb    ext4    defaults    0 0
`'drive/path'    'mount/place'    'Format'    defaults    0 0`

### Storage ->

```
$ ncdu
```

```
$ df '/'
```

```
$ du '/'
```

```
$ free
```


___
# Formating Info
___

Means making a filesystem / VOLUME on a drive giving it an number "E" etc.

#### Common Formats

- NTFS = Windows 
- ext4 = Linux 
- Fat32 = USB