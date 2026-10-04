# Registers & yanky

Neovim has multiple registers. Think of them as several *clipboards*. Most of them are maintained automatically.

To access the registers, hit `"`. A list of the available registers shows up, and you pick the one you need.

- `Space-s"` - friendlier picker for the registers
- `Control-r` - insert from a register while in Insert mode
- `p` - paste in Normal mode

## Common registers

- `+` - system clipboard
- `*` - selection clipboard (on Linux/X11; you can paste it with middle click)
- `_` - *black hole* register. Anything sent here is not saved
- `0` - *last-yanked* register. It is not replaced by deletes, only by yanks
- `.` - *last inserted text*: the text entered during the last Insert mode
- `%` - *current file name* register

## yanky.nvim

Enabled through LazyExtras `coding.yanky`.

- `Space-p` - show the clipboard (yank) history
- `[y` - after pasting, cycle backward through the yank history
- `]y` - after pasting, cycle forward through the yank history
- `[p` - paste one line above, adjusting indentation
- `]p` - paste one line below, adjusting indentation
- `>p` - paste one line below and add indentation
- `<p` - paste one line below and remove indentation
- `>P` - paste one line above and add indentation
- `<P` - paste one line above and remove indentation
