### Show

>\# show vtp { status | counters }

**DTP and VTP are not really used that much because of security risks**

### Turn of DTP

>(int)# switchport mode access `( Static-Access`

or 

>(int)# switchport nonegotiate

### VTP

>(conf)# vtp version 2
>(conf)# vtp domain ccna.com

>(conf)# vtp { Client | Server | Transparent }