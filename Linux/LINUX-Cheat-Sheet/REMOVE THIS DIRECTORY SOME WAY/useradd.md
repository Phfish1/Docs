```
$ useradd [OPTIONS] USERNAME
```

g = main group | username | phfish
G = secondary group. | sudo | wheel
a = append (needed to add multiple groups)
`/etc/group`

m = Make Directory
s = Shell

```
$ useradd -mG sudo -s /bin/bash phfish
```

