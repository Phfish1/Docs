#### SSH

Connect to User/root at ip address
```
$ ssh USER@IP-ADDR
```

``` bash
$ ssh-keygen -t rsa -b
```


$ ssh-copy-id `(Easy key copy "linux")`
>$ scp 'filepath' 'user'@192.168.1.128:/file/path

## Securing SSh

#### Keys

- Permissions [Chmod](/LINUX-Cheat-Sheet/spc/Chmod-X-Chown)
1. .ssh directory [ 700 (drwx------) ]
2. Public-Key .pub [ 644 (-rw-r--r--)]
3. Private-key [ 600 (-rw-------) ]

>$ ssh-keygen -t rsa -b 4096 `Client`
>$ mkdir /home/user/.ssh `Server`
>$ chmod -R 700 .ssh `Server`
>$ scp 'id_rsa.pub' 'user'@192.168.1.128:/home/user/.ssh/authorized_keys `Client`
>$chmod -R 600

>$ ssh 'user'@'ip' -i 'private-key'

#### Config

```ad-example
title: /etc/ssh/sshd_config
collapse: open

PermitRootLogin no
Port 22 `(Can be changed to avoid botting)`
AddressFamily inet `(ipv4 <-- 6)`
PasswordAuthentication no `(Only ssh-key login)`

```

Consider tools like: [ Fail2Ban ] (blocks failed attempt ip addresses)

#### [Firewall](Firewalls%20UFW.md)