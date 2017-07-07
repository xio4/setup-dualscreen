# setup-dualscreen
## Setup 2 monitors with separate screens and common mouse/keyboard

Setup xorg.conf to 2 monitors config.

Remove "ServerLayout" section and create xorg.conf.d/90-main.conf: 

```
Section "ServerLayout"
	Identifier     "Layout0"
	Screen      0  "Screen0" 0 0
	Screen         "Screen1" 0 0
	InputDevice    "Keyboard0" "CoreKeyboard"
	InputDevice    "Mouse0" "CorePointer"
	Option         "Xinerama" "0"
EndSection
```
Compile: [dualscreen-mouse-utils](http://dsp.mcbf.net/releases/dualscreen-mouse-utils-0.5.tar.gz)

Add hotkey to wm: mouse-switchscreen -f 1 
