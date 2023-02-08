### Alacritty

example file: `/usr/share/doc/alacritty/example/alacritty.yml`

**DOOM-ONE** | mkdir |  `~/.config/alacritty/alacritty.yml`
[ConfigFile](https://gitlab.com/dwt1/dotfiles/-/blob/master/.config/alacritty/alacritty.yml)

### Powerline

```
$ pacman -S powerline powerline-fonts 
```

Add | Edit `.bashrc` 
```
powerline-daemon -q
POWERLINE_BASH_CONTINUATION=1
POWERLINE_BASH_SELECT=1
. /usr/share/powerline/bindings/bash/powerline.sh
```
Then `$ source .bashrc`

___

**POWERLINE VIM**
Add this to `~/.vimrc`: ( [Wiki](https://powerline.readthedocs.io/en/latest/troubleshooting.html#vim-issues) ) 
might need to install: `powerline-vim`
```
set encoding=utf-8
python3 from powerline.vim import setup as powerline_setup
python3 powerline_setup()
python3 del powerline_setup
set laststatus=2 " Always display the statusline in all windows
set showtabline=2 " Always display the tabline, even if there is only one tab
set noshowmode " Hide the default mode text (e.g. -- INSERT -- below the statusline)
set t_Co=256
```

___

**Console** [Link](https://phoikoi.io/2016/11/09/powerline-console.html)

Copy Poweline fonts to: `/usr/share/kbd/consolefonts`
```
$ git clone https://github.com/powerline/fonts/tree/master/Terminus/PSF pwline
$ cp -r pwline/*.psf.gz /usr/share/kbd/consolefonts
```
| [[Instalation Common ( 2 ) 22.11.2022#Console| ChangeFont]] | To change fonts