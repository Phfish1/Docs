### Show

>\# Show ip DHCP Snooping **Binding** `( Shows "dhcp-snooping binding table"`

### DHCP-Snooping conf

>(conf)# ip DHCP Snooping 
>(conf)# ip DHCP Snooping vlan 1 `( Config for each vlan`

>(conf)# NO ip DHCP Snooping information option 
`( Needed unless Layer3 switch is dhcp relay agent ("Removes info option  82")`

>(int)# ip DHCP Snoping TRUST `( Apply on int towards Router / DHCP server`

### Snooping Rate-Limit

>(int)# ip DHCP snooping Limit Rate 15 `( 15 DHCP-msg per S`

**ERR-DISABLE**
>(conf)# errdisable recovery cause DHCP-RATE-LIMIT