### Show

>\# show [switch] power inline
># show int g0/0 switchport 

### Power Policing

>(int)# Power inline police
`(err-disable + SysLog)`


>(int)# Power inline police action log
>`(Restart + SysLog)`

___
# VoIP
___

Voice VLAN config

>(int)# switchport access vlan 10 `( Normal VLAN`

>(int)# switchport **voice** vlan 11 `( Voice VLAN`


