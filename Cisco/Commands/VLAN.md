### Access VLANs

>(int)# switchport mode access `( Makes switchport "STATIC ACCESS"`

>(int)# switchport access VLAN 10

Name VLANS
>(conf)# vlan 10
>(vlan)# name Sales


### Trunk Port

>(int)# switchport trunk encapsulation dot1q `( Enables "IEEE 802.1Q" Encapsulation`

>(int)# switchport mode trunk
>(int)# switchport trunk allowed vlans 10,20,30

NATIVE VLAN should be an unused vlan: **1002**-1005

>(int)# switchport trunk native vlan 1002

___
# Inter-VLAN routing
___

### **SVI** Best way

>(conf)# **ip routing** `( Enables ROUTING on a layer 3 switch`

>(conf)# int vlan 10
>(int-vlan)# ip addr 192.168.1.1 255.255.255.192
>(int-vlan)# no shutdown


On the interface FACING the ROUTER

>(int)# **no switchport** `( Makes port layer 3`

>(int)# ip addr 10.0.0.1 255.255.255.252
>(conf)# ip route 0.0.0.0 0.0.0.0 10.0.0.2 `( DEFAULT ROUTE Out of network`


### ROAS ( Router On A Stick )

R1
>(conf)# int g0/0.10
>(int)# encapsulation dot1q 10 `( 10 = VLAN`
>(int)# ip addr 192.168.1.1 255.255.255.192

SW ( Config normal trunk port )

___
# DTP, Dynamic Trunking Protocol
___

**Disable it!!!** ( For security )

> (int)# switchport nonegotiate

___
# VTP, VLAN Trunking Protocol
___

**DONT USE!!!** ( For security + complex/risky)

>\# show vtp status

>(conf)# vtp domain ccna
>(conf)# vtp version ?
>(conf)# vtp mode [client | server | transparent]