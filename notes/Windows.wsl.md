---
id: 2u6lg94vfxyozmorqn8ukk8
title: wsl
desc: ''
updated: 1708084139317
created: 1708080338287
---

## PreRequisites

Install `wsl` from Microsoft store. Or update the current wsl

## Installing A Distribution

On my work machine

```
wsl --install -d Ubuntu
```

> Q: Will it install the latest Ubuntu ?
>> - Yes


### Opening a already present WSL

```ps
wsl
```

## VSCode in wsl

1. Go to VSCode
2. In the command pallete : `WSL: New WSL Window`


> VSCode will give you suggestion to change to wsl2 if you're currently using wsl1

## Change to wsl version 1 to wsl 2

- **wsl2 is the new and recommended version**

Check the version for your linux distribution

```ps
wsl --list --verbose
```

Change the version

```ps
wsl --set-version Ubuntu 2
```

> This conversion may take some time

Restart the PC
