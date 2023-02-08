### Show

>\# show ip ssh

### ConsolePort Security

>(conf)# line console 0
>(line)# password "CCNA"
>(line)# login `( Enables login`

### Users

>(conf)# Username "philip" secret "ccna"
>(line)# Login LOCAL `( Usr + Pas`

### Switch Managment IP

>(conf)# int vlan 1
>(int)# ip addr 192.168.1.1
(int)# no shutdown

>(conf)# IP DEFAULT-GATEWAY 192.168.1.254
`( makes switch able to forward ) Remember to config SSH`

### SSH

**Pre config**

>(conf)# hostname R1
>(conf)# ip domain name philip.com

>(conf)# enable secret
>(conf)# username philip secret ccna

**SSH config**

>(conf)# Crypto key generate rsa 2048 `( 4096`

>(conf)# line vty 0 15 `( 0-15 "all vty lines"`

>(line)#Login LOCAL
>(line)# transport input ssh

**Extra** [ Recomended ]

>(conf)# ip ssh version 2
(conf)# acces-list 1 permit host 192.168.1.1 `( Permits login to only 1 host`

>(line)# acces-class 1 in
>(line)# exec-timeout "MIN" "SEC"