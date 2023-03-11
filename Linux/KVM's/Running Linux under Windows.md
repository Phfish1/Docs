### WSL ( Windows Subsystem for Linux )

WSL is virtualization technology allowing you to run linux directly on top of your windows machine. 

- While still being able to access windows files. 
- And  yes. All linux commands are unmodified.
- use packet managers like apt or pacman

Amazing! for more see [Microsoft: What is WSL2](https://learn.microsoft.com/en-us/windows/wsl/about) 

___

For a more in depth video guide. See [David Bombal WSL](https://www.youtube.com/watch?v=_fntjriRe48) 

To Install do:

```
$ wsl --install
```

Reboot
then install the distro you want

```
$ wsl --install ubuntu
```

doing only `wsl --install` shows you your options

Then simply open PowerShell or CMD and type:

```
$ wsl
```

> Remember to update && upgrade ;)

___

# File management

### `1.1` Windows VS Linux files

**WSL 2 is running as a hyper-v virtual machine** Using custom linux kernel
See [Microsoft: Linux WSL Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) 

Your linux file system is just like normal.

![[LinuxWSL-FileSystem01.png]]

And to access windows files go to `/mnt/[DRIVE]`

![[LinuxWSL-FileSystem02.png]]



### `1.2` Where is the wsl stored?

You can access you linux file system from the wsl command line or through the File Explorer GUI Tabs

![[LinuxWSL-explorer.png]]

Here is where my instance of Ubuntu linux is REALY stored:

``` cmd
C:\Users\Philip\AppData\Local\Packages\CanonicalGroupLimited.UbuntuonWindows_79rhkp1fndgsc\LocalState
```

as a vhdx file: `ext4.vhdx` ( ext4 refering to the filesystem

# WSL integration with VS CODE

You can use VS Code to connect to your linux wsl instance.
"Basicly: Linux terminal under vscode" NICE

- You need to install the WSL Vs Code Extension first.

2 Methods:
___

### `1.` Use CLI to open Vs Code

Opens curent directory. " command Inside wsl instance"
``` bash
$ code .
```

### `2.` Use Vs Code to connect to WSL

Click green button in left corner. -> connect to WSL. Brain happy

![[WSL-vscode01.png]]



# GUI Access

WSL is often only CLI, but a GUI interface is possible in WSL 2

- Ubuntu: (Limited GUI access ) See [WLS 2 GUI](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-11-with-gui-support#5-install-and-use-a-gui-package) or [Microsoft: Ubuntu GUI](https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps) 

- Most Distros: (Full GUI access) [WSL2 With GUI using Xvnc](https://gist.github.com/tdcosta100/385636cbae39fc8cd0937139e87b1c74)  

- **Kali linux** RECOMENDED. Extended GUI acces using **Win-KeX** [Kali-Docs](https://www.kali.org/docs/wsl/win-kex)

___
___

# More commands

To stop wsl instance

```
$ wsl --shutdown
```

list wsl instances and versions

```
$ wsl -l -v
```

WSL update

```
$ wsl --update
```

If you have more than 1 wls instances use:

```
$ wsl -d [DISTRO/NAME]
```

To shutdown(Terminate) spesific wsl instances:

``` bash
$ wsl -t DISTRO
```

# Setting up multiple wsl instances

The simplest way is to install another distribution using the `$ wsl --install DISTRO` command. 
I installed `ubuntu` and `kali-linux`

Then connecting to the them using `$ wsl -d [DISTRO/NAME]`

>You might have to terminate "Restart" the distro. before its fully functional. Remember to update!

To set a default wsl distro: "for when typing `$ wsl`"

``` bash
$ wsl -s DISTRO
```
