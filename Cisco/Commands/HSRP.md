### HSRP ( Hot Standby Reduncancy Protocol )

A FHRP ( First Hop Redundancy Protocol ) Cisco only

SHOW
>\# show standby

R1
>(int)# standby version 2
>(int)# standby 1 ip 192.168.1.252 `( VIP "Virtual IP`

R2
>(int)# standby version 2
>(int)# standby 1 ip 192.168.1.252 `( VIP `

Extra
>(int)# standby 1 priority 200 `( Highest priority becomes ACTIVE`

>(int)# standby 1 preemt `( Forces the router to become always ACTIVE if highest priority`
