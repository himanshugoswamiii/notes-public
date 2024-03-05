---
id: conbwubuf2zou96g2xskq95
title: Wayland
desc: ''
updated: 1709470400856
created: 1709459341955
---

**Find if wayland is running ?**
```bash
$ echo $XDG_SESSION_TYPE
wayland
```

- https://www.baeldung.com/linux/display-server-xorg-wayland

## Clipboard

Install wl-clipboard
```bash
extra/wl-clipboard 1:2.2.1-1
    Command-line copy/paste utilities for Wayland
```

## OBS Studio

Screen not visible when recording  
- *Sol:* Simply change your source to pipewire

![](/assets/images/2024-03-03-15-23-08.png)

## KDE

#### Check which window is using native wayland and which is using xwayland

```bash
qdbus org.kde.KWin /KWin org.kde.KWin.showDebugConsole
```

- https://wiki.archlinux.org/title/Wayland#Kwin_Wayland_debug_console