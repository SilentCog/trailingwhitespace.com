---
title: macOS - i3 on XQuartz
author: mimiflynn
date: 2017-01-07
template: article.jade
---

![i3 Configuration Wizard](images/i3-config-wizard-2-big-select.png)

## Installing i3 on macOS

### Dependencies

[XQuartz](https://www.xquartz.org)

(Homebrew)[https://brew.sh]

### Install i3

`brew install i3`

### Configure i3 as default window manager in XQuartz

```
mkdir ~/.xinitrc.d/
touch ~/.xinitrc.d/99-wm.sh

chmod +x ~/.xinitrc.d/99-wm.sh
```

Open `99-wm.sh` in your favorite text editor and add:
```
#!/bin/sh
exec /usr/local/bin/i3
```

![Start XQuartz](images/start-xquartz.png)

start xQuartz and you will see the following dialog appear from `i3-config-wizard` that runs at first start of i3.

![i3 Configuration Wizard](images/i3-config-wizard-1.png)

![i3 Configuration Wizard](images/i3-config-wizard-2-big.png)

Configure as you would any other way.
