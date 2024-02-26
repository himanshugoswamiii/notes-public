---
id: xl6ynczfz35gmg1yiyfxvfd
title: Helix Editor
desc: ''
updated: 1708980829533
created: 1708967799178
---

- `c` : change 
- `v` : select/extend mode (*extends the selection*)

## Difference

Bad Keybindings in Vim : 
- `ge` why would i use it if i already have `be`

#### Selection `!!important`
- `x` selects a line and press `x` several times to select the lines (forward direction)

#### Deletion 
- `d` deletes everything that is selected

> Cursor is like single character selection

#### Search and Replace

`%sword<Ret>` 
`cReplacement<Esc>`

Explanation: % selects the entire buffer, s opens a prompt for a regex, `<ret>` validates the regex and replace the selection with one per matches (hence, all occurences of word are selected). c deletes the selection contents and enter insert mode, replacement is typed and then `<esc>` goes back to normal mode.

> Imp : Use `,` (comma) to come out of multi selection mode

#### Copy-Paste

`<Space> + p` : to paste from system clipboard
`p` : to paste to helix keyboard
`<Space> + y` : yank to system clipboard
`y` : yank to helix clipboard

---

## Better Things

### Multiple curosrs

Use `C` (Keep pressing it to your position)
Use `,` to get out of mulitple cursor

### Align Selection : Tutor Chapter - 5

---

## Commands to change in neovim

gh : go to the start of the line
gl : go to the end of the line
gd : go to the definition