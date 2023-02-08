### Find int

>$ ls /sys/class/net
>$ ip addr

### setup int

>$ ifconfig wlan0 up
>$nmcli radio on

##### [NetPlan](netplan{D}):
- Can couse issues with interfaces being "Unavailible"
1. Use NetworkManager as a renderer

```ad-example
title: /etc/netplan/conf-wifi.yaml
collapse: open

network:
  version: 2
  renderer: NetworkManager

```
2.
>$ netplan generate
>$ netplan apply
>$ nmcli [radio]

### [Scaning](/Hacking/Information/Scanners)
>$ iwlist wlan0 scan | grep SSID


# Connecting
##### NetworkManager:
>$ nmcli dev status
>$ nmcli dev wifi connect "SSID" password "PASSWORD"
>$ nmcli dev connect wlan0

>$ nmtui `(Graphical)`

- Connecting to [ [WPA-ESP ENTERPRISE](NetworkManager.md) ]



### Disconnecting
>$ nmcli dev disconnect wlan0




# APT
- net-tools
- wireless-tools
- NetworkManager

----
more commands:
iwconfig