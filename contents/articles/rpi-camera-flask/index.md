---
title: Raspberry Pi 3 Camera and Flask
author: mimiflynn
date: 2017-04-03
template: article.jade
---

![fog](images/result.gif)

# RPi 3 Camera

installed latest raspbian

opened ssh port and camera

changed host name to rpi3Cam

changed default password

set up router to reserve ip address via DHCP

SSH into RPi and remove unneeded software

```
sudo apt-get remove --purge wolfram-engine

sudo apt-get remove --purge libreoffice*

sudo apt-get autoremove
```

Set Time

```
sudo dpkg-reconfigure tzdata
```


sudo apt-get remove --purge wolfram-engine penguinspuzzle scratch dillo squeak-vm squeak-plugins-scratch sonic-pi idle idle3 netsurf-gtk netsurf-common

apt-get --purge gnome-* lxde* lightdm* xserver* desktop-* smbclient lxappearance lxinput lxmenu-data lxpanel lxpolkit lxrandr lxsession lxsession-edit lxshortcut lxtask lxterminal leafpad menu menu-xdg xpdf xkb-data xinit xfonts-utils xfonts-encodings xdg-utils xauth xarchiver x11-utils x11-common

https://project.altservice.com/issues/418

Install Vim
```
sudo apt install vim
```

Install NGINX
```
sudo apt install nginx
```

change ssh port to 20002
```
sudo vim /etc/ssh/sshd_config
```

change http port to 2002
```
sudo vim /etc/nginx/site-available/default
```

pull repo into ~/Projects as `Photos` and cd into it

```
mkdir ~/Projects && cd ~/Projects
git clone https://github.com/mimiflynn/rpi-timelapse.git Photos
cd Photos
```

```
mkdir {images,gifs}
```
