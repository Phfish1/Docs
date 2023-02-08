### Creating files

```
$ touch
```

```
$ touch test{0..100} || $ rm test{0..100} 
```

Or use any text editor like
`Nano`, `VIM` or `mousepad`
```
$ vim test.txt
```

### Editing files ->

Echo into file | Add line to file

```
$ echo "Hello" > file || $ echo "hi" >> file  
```

Or of course use Nano VIM etc

### Linking to files ->

Create **symbolic-link** to file

```
ln -s path/old path/symbolic
```
