### Show

>\# Show Port-Security [interface]
>\# Show int g0/0

>\# Show err-disable Recovery

>\# Show mac address-table secure

### Enable Port-Security

>(int)# switchport mode access

>(int)# switchport Port-Security

>(int)# switchport Port-Security mac-addr "A.A.A..." `( Static Port-Security`

### Violation Modes

>(int)# switchport Port-Security violation { Shutdown | Restrict | Protect }

### **err-disable** Recovery

>(conf)# ErrDisable Recovery cause Psecure-violation
>(conf)# ErrDisable Recovery intervall 60 `( Timer MINUTES`

### Aging

>(int)# switchport Port-Security aging type { Absolute | Inacticity }

>(int)# switchport Port-Security aging time 60 `( MINUTES`
>(int)# switchport Port-Security aging static `( Allows static to age`

### Sticky MAC

>(int)# switchport Port-Security mac-address STICKY [MAC]

- Secure/Dynamic MAC-addresses that never age, Basicly static but "Lazy", ( Saved in running-config)


