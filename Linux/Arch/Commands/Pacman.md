### Updating

Update repository & Full-upgrade
```
$ pacman -Syu
```

S = Sync / Download
S**y** = **Update** Package list
S**u** = **Upgrade** all packages

### Instaling

Simply Install
```
$ pacman -S PACKAGE
```

See installed binaries
```
$ pacman -Q | grep INSTALLED
```

See packets to install "Available  in repository"
```
$ pacman -Ss | grep ALL_PACKAGES
```
