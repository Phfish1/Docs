### Config Tunnel gre ( Both sides)

>(conf)# interface tunnel 0 `Enables tunneling interface`

>(int)# tunnel source G0/0/0 `( Interface connected to VPN`

>(int)# tunnel destination 1.1.1.1 `( destination VPN public ip `

**IP for VPN** (Vitrual PRIVATE Network)
>(int)ip addr 192.168.1.1

### Config OSPF between tunnels

First config ospf legit then: (on both routers)
>(ospf)# network "TunnelIP"

Now when you ping the routers subnet (that tunneling was configured on). It will use the VPN Tunnel