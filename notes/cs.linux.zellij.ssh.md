---
id: jb3jf4r8gplsd0n5ojs8t20
title: Ssh
desc: ''
updated: 1709878022954
created: 1709876876822
---

## How does the clipboard copy over SSH ?
It uses OSC52 which can then be sent to the the host machine terminal in which you've opened zellij

> Helix uses `OSC52`

### Neovim problems
- Clipboard doesn't work, because neovim uses xclip or wl-copy. These 2 are used when `$DISPLAY` is set, but in SSH there is no display