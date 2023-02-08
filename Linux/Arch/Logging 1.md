- Document Arch Install
- Document Arch GUI (cinnamon + Lightdm + greeter)
- UEFI vs BOOT
- VNCserver
- Xinit (/etc/X11/xinit/xinitrc >> ~/.xinitrc) [site](https://wiki.archlinux.org/title/Xinit)
- GRUB(Console Res)
- How to edit Grub.cfg (/etc/default/grub && grub-mkconfig -o /boot/grub/grub.cfg) RES (GRUB_GFMODE=1920x1080x32)
- FONTS (ter-d20b.psf.gz) [site](https://unix.stackexchange.com/questions/57085/setting-console-font-in-vconsole-conf-does-not-work-systemd/718654#718654) (FONT MODULE=("VGADRIVER") [Site](https://bbs.archlinux.org/viewtopic.php?id=159195)
- WM(Window Manager) VS DesktopEnviroment [site](https://unix.stackexchange.com/questions/20385/windows-managers-vs-login-managers-vs-display-managers-vs-desktop-environment)
- LightDm [site](https://wiki.archlinux.org/title/LightDM)
- GnomeFix (sudo localedef -f UTF-8 -i en_US en_US.UTF-8) [site](https://stackoverflow.com/questions/24735447/gnome-terminal-doesnt-work-maybe-because-of-locale-setting/41810674#41810674?newreg=f24c06a71a834ed7a39c187c188e49e7)
 
Chris-Titus_Tech: Theme=athier
LIGHTDM CONFIG:
>[Seat:*] 
>**display-setup-script=xrandr -s 1920x1080** 
>greeter-session
>user-session

>$ pacman -Q | grep `(Packages)`
>$ pacman -Ss | grep `(Installed)`


https://phoikoi.io/2016/11/09/powerline-console.html