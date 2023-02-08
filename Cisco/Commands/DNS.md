### SHOW

>\# Show HOSTS

### CMD

>C: ipconfig /all
>C: ipconfig /displaydns
>C: ipconfig /fludhdns `( Flush DNS record`

>C: nslookup "DOMAIN-NAME"

### DNS-Client router

>(conf)# ip domain lookup
>(conf)# ip name-server 8.8.8.8

### DNS-Server router

>(conf)# IP DOMAIN LOOKUP `( Enables DNS Queries`
>(conf)# ip DNS server `( Enables DNS-Server`
>(conf)# ip host youtube.com 192.168.1.100
>(conf)# ip name-server 8.8.8.8 `( Backup`

**Domain**

>(conf)# ip domain name router.com