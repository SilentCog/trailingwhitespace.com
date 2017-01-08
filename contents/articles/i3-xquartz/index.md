---
title: macOS - i3 on XQuartz
author: mimiflynn
date: 2017-01-07
template: article.jade
---

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

start xquartz

Configure as you would any other way.
