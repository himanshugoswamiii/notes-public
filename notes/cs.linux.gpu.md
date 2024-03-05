---
id: n128bg20gy6q4r6eupbvr42
title: Gpu
desc: ''
updated: 1709456841928
created: 1709455058915
---
## Problems with *External Monitor*

### Hybrid Graphics

> Q: Does *logout* works ?
> - Yes (in X11 as well as Wayland)
> But there is a problem that you won't be able to see login screen on external monitor


You can't use sleep
- If you did you won't be able to see the screen when you try to login again

*Error:*

```bash
Mar 03 13:39:57 endeavour kernel: Bluetooth: hci0: unexpected event for opcode 0x0c24
Mar 03 13:39:59 endeavour kernel: amdgpu 0000:05:00.0: [drm] *ERROR* Error queueing DMUB command: status=4
```


- Issue : https://gitlab.freedesktop.org/drm/amd/-/issues/2862