---
title: macOS - i3 on XQuartz
author: mimiflynn
date: 2017-01-07
template: article.jade
---

![i3 Configuration Wizard](images/)i3-config-wizard-2-big-select.png)

## Installing i3 on macOS

### Dependencies

install xquartz - https://www.xquartz.org
install homebrew - https://brew.sh

### Install i3
`brew install i3`

### Configure i3 as default window manager in X11

```
mkdir ~/.xinitrc.d/
touch ~/.xinitrc.d/99-wm.sh

chmod +x ~/.xinitrc.d/99-wm.sh
```

```
#!/bin/sh
exec /usr/local/bin/i3
```

start xquartz

![i3 Configuration Wizard](images/)i3-config-wizard-1.png)

![i3 Configuration Wizard](images/)i3-config-wizard-2-big.png)

Configure as you would any other way.
