### CDP + LLDP

>\# show CDP
>\# show cdp NEIGHBORS
>\# show cdp Traffic
>\# show cdp interface [detail]

>\# show cdp neighbors detail
>\# show cdp entry "DEVICE-ID" `R1`

### CDP conf

>(conf)# [no] cdp run
>(int)# [no] cdp enable

### LLDP conf

>(conf)# LLDP run
>(int G0/1)# LLDP transmit 
>(int G0/1)# LLDP receive


### Timers

>(conf)# cdp Timer "seconds"
>(conf)# cdp HoldTime "secconds"