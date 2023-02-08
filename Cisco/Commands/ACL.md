### Show

>\# show ip access-list ["NAME"]

uses **Wildcard masks!**

### Standar ACL [ NAMED ]

Numbered (1-99, 1300-1999)

>(conf)# IP access-list standard acl1
>(acl)# permit 192.168.1.0 0.0.0.255
>(acl)# permit any any

# Extended

Numbered (100-199, 2000-2699)

>(conf)# ip access-list extended acl2
>(acl)# 10 permit 192.168.1.0 0.0.0.255 any host 192.168.2.100 eq 443 
`( Permits 192.168.1.0/24 to access host 192.168.2.100 on port 443(HTTPS)`
` 10: specifies entry 10 | Any: any source ports | Host: specifies single host

>(acl)# no 10 `( DELETE access-list entry 10`

___

>(acl)# resequence acl1 10 10 `( Sets first entry: 10, Every after that to: 10`
