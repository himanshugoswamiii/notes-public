---
id: gifvyk24oehjtxf42gimji8
title: Nvidia
desc: ''
updated: 1709450514697
created: 1709450201399
---

*Install `envycontrol` from AUR*
- https://github.com/bayasdev/envycontrol
## Check which drivers are running ?
```bash
$ envycontrol --query
hybrid
```

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
