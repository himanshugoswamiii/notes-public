---
id: lwp71fnv8089oa1fzcw11kd
title: nnn
desc: ''
updated: 1708490732416
created: 1708451272747
---

Install all the plugins :
- https://github.com/jarun/nnn/tree/master/plugins

The command to install is given it'll automatically install in `~/.config/nnn/plugins`

### Copy selection path to clipboard

1. Install all the plugins
2. Run `nnn -x` 

If you want this behavior permanently add it to `~/.config/zsh/nnn.zsh`

### Drag and Drop

See the plugin : `dragdrop`

## Plugins

Access the plugins by pressing `;` then the key you set in your configuration

### preview-tui

##### 1. Add the following to your `nnn.zsh`

```bash
export NNN_FIFO="/tmp/nnn.fifo"
export NNN_PLUG="t:preview-tui"
```
##### 2. For using this with kitty terminal, set the following lines to `kitty.conf` :

```bash
allow_remote_control yes

###

listen_on unix:/tmp/mykitty
```





