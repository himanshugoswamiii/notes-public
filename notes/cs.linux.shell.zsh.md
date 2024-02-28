---
id: is1nd6u1z2kcproc6mhsljz
title: Zsh
desc: ''
updated: 1709135823066
created: 1709133098159
---

## History

Check if the history file is availbe 
```bash
echo $HISTFILE
```

To save `zsh` history add the following lines to your `.zshrc`

```bash
export HISTFILE=~/.zsh_history
export HISTSIZE=1000
export SAVEHIST=1000
```

> Now, source `.bashrc` and then close and open the terminal  
>  run the `echo $HISTFILE` command to see if the file is created

**How to search through the history ?**
- `<ctrl> + r`

> For better history look at [[fzf-command-history|cs.linux.cli-tools.fzf#fzf-to-search-commands-history]]

---

## Reference
- https://linuxhint.com/check-zsh-history/