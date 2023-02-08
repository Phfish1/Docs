### Show

>\# show ip NAT Translation
>\# show ip NAT Statistics

### Managment

>\# clear ip NAT Translations * `( Clears dynamic translations`

### Static NAT

>(int-G0/1)# ip NAT Inside `( LAN interface`
>(int-G0/0)# ip NAT Outside `( WAN interface`

>(conf)# ip NAT inside source static "inside-local" "inside-global"
>`(192.168.1.1 203.0.113.1), NAT Translation`

### Dynamic NAT

>(int-G0/1)# ip NAT inside
>(int-G0/0)# ip NAT outside

**ACL** (specifies subnet to be translated)
>(conf)# access-list 1 permit 192.168.1.0 0.0.0.255

**Pool**
>(conf)# ip NAT pool "POOL_NAME" 100.0.0.1 100.0.0.10 prefix length 24

**DYNAMIC NAT**
>(conf)# ip NAT inside source List "1" Pool "POOL_NAME"

---
---

# **PAT** (Port Address Translation)

---
---

### Public IP (interface) "IP SAVING"

>(int-G0/1)# ip NAT inside
>(int-G0/0)# ip NAT outside

Decides who are eligable for NAT/PAT
>(conf)# access-list 1 permit 192.168.1.0 0.0.0.255

**PAT**
>(conf)# ip NAT inside source list 1 **Interface G0/0 OVERLOAD** `( Outside nat interface`

### PAT using Pools. Extra IPs needed

>(int-G0/1)# ip NAT inside
>(int-G0/0)# ip NAT outside

ACL for elegible for NAT/PAT
>(conf)# access-list 1 permit 192.168.1.0 0.0.0.255

NAT Pool where extra IPs are defined
>(conf)# ip NAT pool "POOL_NAME" 100.0.0.1 100.0.0.254 prefix-length 24

**PAT**
>(conf)# ip NAT inside source list 1 pool "POOL_NAME" **OVERLOAD**

### Port forwarding

>ip nat inside source static **tcp** 192.168.1.100 **80** 10.0.0.1 **80** 

- ( Inside ip address 192.168.1.100 on port 80. | Translate to 10.0.0.1 port 80

So when anyone tries to connect to 10.0.0.1(Router) on port 80 they will be forwarded to 192.168.1.100(Server) on port 80