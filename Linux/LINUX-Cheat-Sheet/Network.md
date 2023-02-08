# `1` General

```
$ ip addr
```

### `1.1` DNS

DNS server
```
$ cat /etc/resolv.conf
```

Resolves DNS, See [host](https://www.computerhope.com/unix/host.htm)
```
$ host google.com
```

DNS Info
```
$ resolvectl status
```

# `2` Network Managing

```
$ systemctl start NetworkManager
```

```
$ nmcli
```

### `2.1` WiFi

See [ArchWiki](https://wiki.archlinux.org/title/NetworkManager) for a great explaination

```
$ nmcli device wifi list
```

```
$ nmcli device wifi connect SSID password PASSWORD
```


**To connect to Enterprise networks see [[Network#`4.1` Connecting to enterprise networks]]**

### `2.2` Network traffic

```
$ netstat
```

```
$ ss
```

Alternatively use a packet analyzer like wireshark

# `3` Firewall

Iptables or UFW

```
$ ufw allow 22
```

```
$ ufw enable
```


# `4` Testing

`-c` = count 
`-s` = size in bytes

```
$ ping -c 3 -s 1000
```

```
$ traceroute 1.1.1.1
```


___
# `5` Extra info
___

### `5.1` Connecting to enterprise networks

NetworkManager can be used through the CLI 
`$ nmcli`, or a limited TUI version can be accesed through the 
`$ nmtui` command

For Enterprise connection we need to edit the NetworkManager configuration.

### `5.1.1` FilePaths

```
/etc/NetworkManager/system-connections
```

### `5.1.2` Editing configuration

This step might a bit confusing. to learn more check out this -> [Video](https://www.youtube.com/watch?v=wHXKo9So5y8) On wireless security.
or for some quick info see [askubuntu](https://askubuntu.com/questions/262491/connect-to-a-wpa2-enterprise-connection-via-cli-no-desktop)


Add the connection
```
$ nmcli connection add type wifi ifname "INTERFACE" con-name "CONNECION-NAME" ssid SSID
```

Edit the connection config
```
$ ncmli connection edit id "CONNECTION-NAME"
```

You will now enter *nmcli interactive connection editor*
do the following

___

```
nmcli> set ipv6.method auto
```

The eap method migh be diffrent depending on your orgonization peap is the most common
```
nmcli> set 802-x.eap peap
```

MS-CHAPv2 stands for *Microsoft Challenge Handshake Authentication Protocol*
```
nmcli> set 802-1x.phase-auth mschapv2
```

Most likelly email
```
nmcli> set 802-1x.identity USERNAME
```

```
nmcli> set 802.1x.password PASSWORD
```


**Commands you also migh need**

-   `nmcli> set wifi-sec.key-mgmt wpa-eap`
-   `nmcli> set 802-1x.password PASSWORD`
-   `nmcli> set 802-1x.anonymous-identity ANONYMOUS-IDENTITY`

To save do

```
nmcli> save
```

```
nmcli> activate
```