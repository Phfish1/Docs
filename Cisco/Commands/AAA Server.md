AAA Servers:
1. Tacacs+
2. RADIUS

We will be using Tacacs+, since it is mainly used for administration of nodes(network devices)

Config AAA Server on a Server.

![[AAA01.webp]]

## Commands

Enables AAA. and deletes old AAA commands
>(conf)# aaa new-model

Enables AAA for enable secret
>(conf)# aaa authentication enable default group tacacs+ [local]

>(conf)# aaa authentication login default group tacacs+ [local]

Configure the client with tacacs server ip and key
>(conf)# tacacs-server host 10.0.0.100 key ccna

___

`enable / login` = Leting AAA server decide enable / login secret and password

`default` = authentication list

`group tacacs+` = Where to get the password / username from

`local` = where to get backup username and password if tacacs+ server is down


