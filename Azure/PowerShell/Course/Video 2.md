### Important

Alias = -> ? <-
```
> Where-Object {}
```

Only return when $\__. free is greater than 1
```
> Get-PSDrive | Where-Object {$_.Free -gt 1}
```

-> **$__** <- Means current object in **Pipe**

Selects objects from pipe | Use -> `*` <-
```
> Get-PSDrive | Select-Object Root, Free, Used
```

Does a loop for each object 
```
> ForEach-Object {}
```

Writes on screen for each object
```
> ForEach-Object {Write-Host $_.Root "Free:" ($_.Free /1gb) "Used:" ($_.Used /1gb)  -Seperator " | " -ForegroundColor Cyan} 
```
Divided by 1GB
`"{0:N2}" -f` Formats number to "0,00"

```
Get-PSDrive | Where-Object { $_.Free -gt 1} | ForEach-Object {Write-Host $_.Root "Free:" ("{0:N2}" -f ($_.Free /1gb)) "Used:" ("{0:N2}" -f ($_.Used / 1gb)) -Separator " | " -ForegroundColor Cyan}
```

___

Do first only at start middle for each object and last for last object
```
ForEach-Object {"Hello"} {"Hi"} {"Bye"}
```

___

Spits out Where the **object** definition is equal to "ForEach-Object"
```
> Get-Alias | Where-Object {$_.Definition -eq "ForEach-Object"}
```

___
___

```
> Get-PSDrive
```

```
> Get-Volume
```