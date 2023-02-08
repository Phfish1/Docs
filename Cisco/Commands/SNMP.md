### SNMP (AGENT)

### Show

>\# show snmp


### SNMP

>(conf)# **snmp-server community "password" {ro | rw}** 
>`(Read-Only | Read/Write)`

>(conf)# snmp-server host "NMS ip" version "2c" "password"
> `( "community-string" NMS:(Network Managment Server)`

>(conf)# snmp-server enable traps snmp linkup linkdown 
>`( Enables trap msg to be sent on certain conditions`

Extra

>(conf)# snmp-server {conntact | location} "string" `(Optional)`
