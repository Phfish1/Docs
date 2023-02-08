Always run in **Administrator-Mode**

**Keeps Log**

```
> Start-Transcript
```

___

Get Command

```
> Get-Command {-Noun "" | -Name "Get*" | -CommandType ""}
```

-A lot of GET commands

### Get-Help

Updates Help list

````
> Update-Help
````

```
> Get-Help "COMMAND" [ -Examples ]
```
f.eks *Get-Help Get-Service* || All commands have Help and Examples

**ONLINE**

```
> Get-Help "COMMAND" -Online
```

____

### Aliases

Powershell uses Aliases to shorten commands. For **learning dont use them**
f.esk | ls -> Get-ChildItem | dir -> Get-ChildItem | rm -> Remove-Item

```
> Get-Alias "Alias"
```

Alias = ls | rm | dir | cls | clear

Reverse Output

```
> Get-Alias | where {$_.Definition -eq "Get-ChildItem"}
```

___
___

### Process

```
> Get-Process
```

```
> Get-Member
```

-> | <- Pipe takes the **output of command** and takes **Object** over to other side

```
> Get-Process -Name Discord | Get-Member [-MemberType Method]
```

Get-Member <- | Gets **Properties** and **Methods** of Object

```
> Get-Process -Name Discord | Select-Object *
```

Select The **Object** from Get-Member command
- Select-Object ID
- Select-Object * `<-- Everything`

____

### Variables

```
> $phfish = Get-Process notepad
```
Always do 
- **$phfish** | Test the variable. No Typos'

```
> $variable
```

**Acess Methods** and **Properties**

```
> $variable.kill()
> $variable.name

> $variable.method()
> $variable.propertie
```

____

### History and such

```
> Get-history
```

Transcript File | ``C:\Users\Philip\Documents``
- **Documents** Folder



