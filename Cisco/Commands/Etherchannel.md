### Show

>\# show etherchannel summary
>\# show eterchannel port-channel
>\# show etherchannel load-balance

### Etherchannel **LACP**

>(int-range)# channel-group 1 mode active `( Active = LACP`
>(int-range)# channel-protocol LACP

>(conf)# int port-channel 1
>(int)# switchport mode trunk

### Load-Balancing

>(conf)# port-channel load-balance "METHOD" `( Method: "src-dst-mac"`


