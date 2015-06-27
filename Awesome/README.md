Awesome
---
Display version
```sh
awesome -v
```
#### Changed shorcuts
Kill window (instead of Mod4 + Shift + c)
```sh
Mod4 + c
```

#### Xephyr
Installation
```sh
sudo apt-get install xserver-xephyr
```
Run
```sh
Xephyr -ac -br -noreset -screen 800x600 :1
```

```sh
Xephyr :1 -ac -br -noreset -screen 900x300 & DISPLAY=:1.0 awesome -c ~/.config/awesome/rc.test.lua &
```
