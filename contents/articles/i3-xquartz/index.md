# installing i3 on macOs

install xquartz
install homebrew

brew install i3

mkdir ~/.xinitrc.d/
touch ~/.xinitrc.d/99-wm.sh

chmod +x ~/.xinitrc.d/99-wm.sh

start xquartz
