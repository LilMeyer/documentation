Awesome
---
Display version
```sh
awesome -v
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

References
---
- [Debugging](https://wiki.archlinux.org/index.php/Awesome#Debugging_rc.lua)
- [Shortcuts](https://awesome.naquadah.org/doc/manpages/awesome.1.html)
- [Volume and control display](https://awesome.naquadah.org/wiki/Volume_control_and_display)
- [Xephyr](https://awesome.naquadah.org/wiki/Using_Xephyr)
