
### Show

>\# show ipv6 ip int b
>\# show ipv6 route
>\# show ipv6 neighbors

### **Important**

>(conf)# IPv6 unicast-routing `( Enables IPv6 unicast ->routing<-`


___
# IPv6 addressing
___

### Manual

>(int)# ipv6 addr 2001:8db::1/64

### EUI-64

>(int)# ipv6 addr 2001:8db::/64 EUI-64 `( Configures host part based on MAC addr`

### SLAAC ( Stateless Address Auto-Config )

enables hosts to get ipv6 addresses Using RS(Router solicitation) and RA(Router advertisment) "Here is our prefix" **Do after configuring EUI-64**

Needed for SLAAC
>(conf)# ipv6 unicast-routing

>(int)# ipv6 addr autoconfig `( Enables hosts to autoconfig ipv6 addresses `

### Link-local 

>(int)# ipv6 enable `( enables ipv6 and generates link-local ip "FE80:: EUI-64"`

### Anycast

>(int)# ipv6 addr 2001:8db::ABCD:99/128 anycast `( one -> one of many "128 = host"`

___
# IPv6 Routing
___

# Network Route

>(int)# ipv6 addr 2001:db8::/64 2001:db8:1::1

Or if configuring with LINK-LOCAL addr

>(int)# ipv6 addr 2001:db8::/64 gigabitEthernet 0/0/1 FE80::A:B:C:D `( FULLY SPECIFIED Route`

### Floating Static

>(int)# ipv6 route { IPv6 ADDR } { IPv6 "VIA" ADDR } 111 `( 111 = AD(Administrative Distance)`

### Default route

>(int)# ipv6 route ::/0 2001:db8::1