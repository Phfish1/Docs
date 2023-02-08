# SystemStatus



>$ [h]top

- POWER:
>$ cat /sys/class/power_supply/BAT0/capacity
>$ acpi
>$ upower [-d]

### Distro

```
$ uname -r
```

more info

```
$ cat /etc/os-release
```

```
$ lsb_release -a
```

### Processes

```
$ ps -aux
```

```
$ pkill -f NAME || kill -9 ID
```


### Specs

>$ hwinfo [ --short ]
>$ lshw `(LiSt HardWare), (-short)`

### GPU

>$ lspci [-v]  [-s]  `(--Verbose), (select {00:1f.3} # ID #)`
>$ nvidia-detect
>$nvidia-smi

><b>Benchmark</b>
>$ hashcat -b


### USB

>$ lsusb


##### APT

- SystemStatus:[ htop ]
- GPU:[ nvidia-cuda-toolkit | nvidia-driver ] `(# to install drivers #)`
- Benchmark:[ Hashcat ]
- Power:[ acpi ]