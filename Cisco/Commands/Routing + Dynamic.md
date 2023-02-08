
### Static

> (conf)# ip route 192.168.2.0 255.255.255.0 172.16.14.4 `( Get to 192.168.2.0/24 VIA 172.16.14.4`

### Switchport

>(int)# no switchport `( Makes switchport layer 3`

>(conf)# ip routing `( Enables layer 3 switch to route`

___
# Dynamic Routing
___

### Shows

>\# **show ip protocols**
>\# show ip ospf neighbours
>\# show ip ospf int { brief | g0/0 }
>\# show ip ospf database

### Floating static "Backup route"

> ip route 192.168.2.0 255.255.255.0 10.0.0.2 120 `( 120 = AD`

### **IMPORTANT**

Config-Router = OSPF / EIGRP / RIP

Configure a loopback interface for a reliable RID ( Router ID )

>(conf)# int loopback1
>(int)# ip addr 1.1.1.1 255.255.255.255

>(Config-Router)# passive-interface { g0/1 | loopback 1 }  `( Interface to switch | No unesacary traffic`

>(Config-router)# default-information originate `( Shares default route AKA connection out from the Enterprise --> Internet`

>(Config-router)# distance 90 `( -> AD <- of the protocol instance`


___
## OSPF
___


>(conf)# router ospf 1

>(ospf)# network 10.0.0.0 0.0.0.3 area 0
>(ospf)# network 192.168.1.0 0.0.0.255 area 0

Needed if GigabitEthernet should have less METRIC than FastEthernet ( Else both = 1 )

>(ospf)# **auto-cost reference-bandwidth 100000** `( Makes OSPF METRIC Future proof,`


passive-interfaces [ ->switch, loopbacks ]

>(ospf)# passive-interface default `( suppress all`
>(ospf)# no passive-interface G0/0 `( On router OUT interface`

Priority ( Who becomes DR and BDR )

>(int)# ip ospf priority 255

See [Serial](Commands/Serial) For OSPF *PPP* connection
And also apply this command to tell OSPF its a point-to-point connection
>(int)# ip ospf network point-to-point


Neighbor command for NonBroadcast networks. For **Non-Broadcast** OSPF
>(ospf)# neighbor { IP-ADDR } [cost]

### Troubleshooting

**Timers**

>(int)# ip ospf { hello | dead }-interval 20

Authentication

>(int)# ip ospf authentication-key ccna
>(int)# ospf authentication

ospf network mismatch [Serial](Commands/Serial)

>(int)# no ip ospf network

___
## EIGRP
___

>(conf)# router EIGRP 1 `( 1 = AS "Must Match between all routers"`

>(EIGRP)# no auto-summary `( Enables CIDR`
>(EIGRP)# network 10.0.0 0.0.0.3
>(EIGRP)# network 192.168.1.0 0.0.0.255

EIGRP Unequal-cost load-balancing

>(EIGRP)# varience 2