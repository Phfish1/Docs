### Show

>\# show ip ARP Inspection interfaces
>\# show ip ARP Inspection

### DAI Conf

>(conf)# ip ARP Inspection vlan 1 Trust

>(int)# ip ARP Inspection Trust

### Rate-Limit

>(int)# ip ARP Inspection Limit-Rate 15 [burst interval 2] `( 15 arp per 2 sec`

ERR-DISABLE
>(conf)# errdisable recovery cause ARP-Inspection

### Optional Checks

>(conf)# ip ARP Inspection Validate dst-mac src-mac ip `( For all checks`

### ARP ACL

>(conf)# APR acces-list acl-name
>(ARP-ACL)# Permit IP host 192.168.1.100 MAC host AAAA.BBBB.CCCC

>(conf)# ip ARP Inspection Filter acl-name vlan 1