### SHOW

>\# show DHCP binding
>\# show IP dhcp "?"

### CMD

>C: ipconfig /all
>C: ipconfig /release `( Expire DHCP lease`
>C: ipconfig /renew

___
### DHCP router
___

>(conf)# ip dhcp  excluded-address 192.168.1.1 192.168.1.10
>`Excludes ip addr 1 - 10`

>(conf)# ip dhcp pool "name"

>(dhcp)# Nettwork 192.168.1.0 { /24 | 0.0.0.255 } 

>(dhcp)# Default-router 192.168.1.1
>(dhcp)# DNS-server 8.8.8.8
>(dhcp)# Domain-name philip.com

>(dhcp)# lease 0 12 30 `( "DAYS" "HOURS" "MIN"`

### DHCP **Relay**

>(conf)# int G0/1 
>`interface on DHCP CLIENTS subnet ( 192.168.1.0/24 ) not facing server`

>(int G0/1)# ip helper-address 192.168.1.1 `( dhcp SERVER ip`