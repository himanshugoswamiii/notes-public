---
id: y9pod28b15404bvzfvaqp83
title: fzf
desc: ''
updated: 1708506246581
created: 1708453817719
---

## Installation

```bash
sudo pacman -S fzf
```

Note: You may not have *fuzzy completions* enabled by default

*Solution:* Add the following to your `.zshrc` :

```zsh
# fzf completions
if [ -f /usr/share/fzf/completion.zsh ]; then
    source /usr/share/fzf/completion.zsh
fi
```

Reference : https://wiki.archlinux.org/title/fzf

## Usage

#### To fuzzy find
```bash
nvim -o `fzf`
```

or

```bash
nvim -o $(fzf)
```

This will find the files and when you select that file it'll open in neovim

> **Note:** The second syntax is generally recommended

#### Exact match

```bash
nvim -o `fzf --exact`
```

*or*

Alternatively (with the fuzzy find), prefix a search term with a single quote, like 'string, to opt for exact matches only

```
'string
```

![Image: fzf](/assets/images/2024-02-21-00-09-51.png)

#### cd to any directory
- This will only be available if you've `/usr/share/fzf/completion.zsh` setup to your `.zshrc`

```bash
cd **<TAB>
```

> Note: You don't have to write `<TAB>`, just press it

---

## Reference

- https://www.freecodecamp.org/news/fzf-a-command-line-fuzzy-finder-missing-demo-a7de312403ff/