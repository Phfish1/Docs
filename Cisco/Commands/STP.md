### Show

>\# show spanning-tree
>\# show spanning-tree detail
>\# show spanning-tree vlan 1

# STP conf

>(int)# spanning-tree vlan 1 cost 200 `( Cost of interface when forwarding`

>(conf)# spanning-tree vlan 1 priority 4096 `( Bridge ID / Priority of switch`

### Rapid-STP link-types

link-type Shared. Are all about interfaces connected to hubs

>(int)# spanning-tree link-type { point-to-point | shared }

___
# PVST ( Per VLAN Spanning-tree )
___

On root bridge for VLAN 1

>(conf)# spanning-tree vlan 1 root primary

On BACKUP Root for vlan 1

>(conf)# spanning-tree vlan 1 root secondary


___
# STP Toolkit
___

### Portfast

>(int)# spanning-tree portfast
>(int range)# såanning-tree portfast

### BPDU Guard

>(int range)# spanning-tree BPDUguard enable

>(conf)# spannint-tree portfast BPDUguard default

