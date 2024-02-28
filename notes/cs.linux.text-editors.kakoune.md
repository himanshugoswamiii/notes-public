---
id: 8qe8frohst95oy60jdtw14f
title: Kakoune
desc: ''
updated: 1709112998078
created: 1708977366038
---

```bash
sudo pacman -S kakoune
```

## Usage

```bash
kak filename
```

## Difference with Vim
- *Split windows*, *tabs* and such are left to the WindowManager, terminal emulator or screen/tmux

### Selecting the code completion:
`<Ctrl>+n`

## Configuration

- File : `$HOME/.config/kak/kakrc`

#### Use `<tab>` for completion

```bash
hook global InsertCompletionShow .* %{
    try %{
        # this command temporarily removes cursors preceded by whitespace;
        # if there are no cursors left, it raises an error, does not
        # continue to execute the mapping commands, and the error is eaten
        # by the `try` command so no warning appears.
        execute-keys -draft 'h<a-K>\h<ret>'
        map window insert <tab> <c-n>
        map window insert <s-tab> <c-p>
        hook -once -always window InsertCompletionHide .* %{
            unmap window insert <tab> <c-n>
            unmap window insert <s-tab> <c-p>
        }
    }
}
```

