### Distro info

```
$ uname -all || $ uname -r
```

Or for more distro info
```
$ cat /etc/os-release
```

**Users**

```
$ whoami
```

```
$ id USER
```

```
$ finger USER
```

```
$ groups
```

**AddUser EZ**

```
$ adduser phfish
```

[UserAdd](useradd.md) ( Sudo )

```
$ useradd -mG sudo -s /bin/bash phfish 
```

UserMod
```
$ usermod -G sudo phfish
```

Password
```
$ passwd USERNAME
```
`/etc/paswd`

Create Groups `/etc/group`
```
$ groupadd superhero 
```

```
$ groupdel superhero
```

Common groups
`audio,video,network,sudo,storage,rfkill`

### [Perms](Chmod-X-Chown.md)

```
$ chmod +x file.sh
```

```
$ chown phfish file.sh
```