---
title: Raspberry Pi HiFi DoDad Thingy
author: mimiflynn
date: 2016-03-26
template: article.jade
---

Things:

Raspberry Pi 2
Hifiberry Digi+
SD Card
Anker 5 port USB charger
DAC


## Install Raspbian

Use the [HiFiBerry Installer](https://www.hifiberry.com/guides/hifiberry-installer/) to load up your SD card with a compatible Raspbian image.

I had a little bit of trouble figuring out which output to select in the audio settings. Ended up that optical is Aif.

## Remove unneeded packages
```
sudo apt-get remove --purge minecraft-pi python-minecraftpi
sudo apt-get remove --purge python-pygame python3-pygame
sudo apt-get remove --purge python-numpy
sudo apt-get remove --purge python-tk python3-tk
sudo apt-get remove --purge timidity
sudo apt-get remove --purge scratch nuscratch
sudo apt-get remove --purge libreoffice*
sudo apt-get remove --purge wolfram-engine
sudo apt-get remove --purge oracle-java8-jdk
sudo apt-get remove --purge sonic-pi smartsim penguinspuzzle dillo x2x
sudo apt-get remove --purge python3-pifacecommon python3-pifacedigitalio python3-pifacedigital-scratch-handler python-pifacecommon python-pifacedigitalio
```

## Install

I always add my own bash configuration files with this one simple trick:

```
sh <(curl https://gist.githubusercontent.com/mimiflynn/9144157/raw/25d87a81257008a77aa2f435af59a94204af3c82/install.sh -L)
```

`sudo rpi-update`

Restart with

`sudo shutdown -r now`

```
sudo apt-get update
sudo apt-get upgrade

sudo apt-get install kodi
sudo apt-get install vlc

sudo apt-get install xscreensaver
```




`lcd_rotate=2`

/boot/config.txt


shut down and restart
sudo shutdown -r now

shut down and stay down
sudo shutdown -h now
