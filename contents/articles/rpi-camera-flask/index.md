---
title: Raspberry Pi 3 Camera and Flask
author: mimiflynn
date: 2017-04-03
template: article.jade
---

![fog](images/result.gif)

In an attempt to learn Python, I created a Flask app to control my Raspberry Pi 3 and Pi Camera from my web browser to create time lapses and single photos.

[Check out the code on GitHub](https://github.com/mimiflynn/rpi-timelapse).

## RPi 3 Camera

Attach camera to Pi via ribbon cable and set it up somewhere nice.

Install latest Raspbian (I used noobs to do this, so easy).

## Raspberry Pi 3 Config

Go to the Pi menu and click on settings and then go to config

Open ssh and camera services

Change host name to rpi3Cam

Now that SSH is active you must change the default password with `passwd`

## Set Time on Pi

```
sudo dpkg-reconfigure tzdata
```

## Router Settings

Set up router to reserve ip address via DHCP for the Pi in order to use the same IP address internally for SSH and HTTP access.

## Raspberry Pi Software

SSH into RPi and remove unneeded software. I referenced a [random BB thread](https://project.altservice.com/issues/418).

```
sudo apt-get remove --purge wolfram-engine

sudo apt-get remove --purge libreoffice*

sudo apt-get remove --purge libreoffice* wolfram-engine scratch squeak-plugins-scratch squeak-vm penguinspuzzle dillo sonic-pi idle idle3 netsurf-gtk netsurf-common

sudo apt-get autoremove
```

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

## NGINX

```
cd /etc/nginx/sites-available
sudo vim default
```

Use the below configuration:

```
server {
	listen 2002 default_server;
	listen [::]:2002 default_server;

	index index.html index.htm index.nginx-debian.html;

	server_name localhost;

	# Set up proxy for Flack app
	location / {
		proxy_set_header X-Real-IP $remote_addr;
		proxy_set_header X-Forward-Fo $proxy_add_x_forwarded_for;
		proxy_set_header Host $http_host;
		proxy_set_header X-Nginx-Proxy true;
		proxy_pass http://127.0.0.1:5000;
		proxy_redirect off;
	}
}
```

## Install and setup Flask web camera interface

Clone the repo into ~/Projects as `Photos` and cd into it
```
mkdir ~/Projects && cd ~/Projects
git clone https://github.com/mimiflynn/rpi-timelapse.git Photos
cd Photos
mkdir {images,gifs}
```

Start the app with `nohup python3 app.py &' and go to the server IP address in your browser.
