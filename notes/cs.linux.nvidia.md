---
id: gifvyk24oehjtxf42gimji8
title: Nvidia
desc: ''
updated: 1709450915359
created: 1709450201399
---

*Install `envycontrol` from AUR*
- https://github.com/bayasdev/envycontrol
## Check which drivers are running ?
```bash
$ envycontrol --query
hybrid
```
## Change graphics card to integrated
```bash
$ sudo envycontrol -s integrated
[sudo] password for hg: 
Switching to integrated mode
Successfully disabled nvidia-persistenced.service
Rebuilding the initramfs...
Successfully rebuilt the initramfs!
Operation completed successfully
Please reboot your computer for changes to take effect!
```

> Note: *External screen* won't work with this in Asus TUF (it could be that HDMI output is using Nvidia GPU)
