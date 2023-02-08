### Kill process

1.
```
> Get-Process | Where-Object {$_.ProcessName -eq "Discord"} | kill
```

2.
```
> Get-Process -Name dis* | kill
```

3.
```
> Kill -Name Dis*
```

