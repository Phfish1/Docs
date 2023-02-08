### Read long outputs

```
$ more
```

```
$ less
```

```
$ head || tail
```

-e = Ignore case | -i = noncase 
```
$ grep [-i]  [-e] "-test"
```

Compare && Difference || cmp = where | diff = what
```
$ cmp || diff FILE1 FILE2
```

### Screen

Creates more terminals

```
$ screen -S "name" 
```

```
$ screen -ls
```
`( CTRL + A +D ) ## to detach ##`

```
$ screen -r {'name' | 'id'}
```

```
$ pkill screen `(Kills all)`
```

### Jobs ->

**`( CTRL + Z )`** Puts job into background

```
$ jobs
```

Foreground
```
$ fg 1
```

Background cli
```
>$ bg 1
```

```
$ kill %1
```


