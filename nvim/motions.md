# Motions, modes & search

## Modes

- `i` - enter Insert mode, before the cursor
- `I` - enter Insert mode, at the beginning of the line
- `a` - enter Insert mode, after the cursor
- `A` - enter Insert mode, at the end of the line
- `o` - enter Insert mode, one line below
  - In Visual mode, it switches the selection to the other side
- `O` - enter Insert mode, one line above
- `gi` - go to the last Insert position
- `v` - enter Visual mode
- `V` - select the current line in Visual mode
- `Control-v` - Visual block mode
- `gv` - reselect the last Visual selection
- `Shift-:` - enter Command mode
- `s` - enter Flash mode (plugin: `flash.nvim`). Type a few characters and jump to the label shown
- `S` - Flash treesitter selection (plugin: `flash.nvim`) > [!WARNING] verify

## Motion & navigation

- `$` - move to the end of the current line
- `0` - go to the beginning of the line
- `_` - go to the first non-blank character of the line
- `g_` - go to the last non-blank character of the line
- `w` - move by word
- `W` - move by WORD (whitespace separated)
- `e` - move to the end of the current word
- `ge` - move to the end of the previous word
- `(` - move to the previous sentence
- `)` - move to the next sentence
- `%` - move to the matching bracket
- `gg` - go to the beginning of the file
- `G` - go to the end of the file
- `Count-G` - go to line `Count`

### Repeating find / till

- `;` - repeat the last `f`, `F`, `t` or `T` in the same direction
- `,` - repeat the last `f`, `F`, `t` or `T` in the opposite direction

### Word under cursor

- `*` - search forward for the word under the cursor
- `#` - search backward for the word under the cursor

### Jumps

- `Control-o` - jump backward in the jump list
- `Control-i` - jump forward in the jump list

### Scrolling

- `Control-d` - scroll down (half window)
- `Control-u` - scroll up (half window)
- `Control-f` - scroll forward (one window)
- `Control-b` - scroll backward (one window)
- `Control-y` - scroll up (one line)
- `Control-e` - scroll down (one line)

### `z` commands

- `zt` - move the current line to the top of the window
- `zb` - move the current line to the bottom of the window
- `zz` - move the current line to the middle of the window

## Find & till

- `f{char}` - move to the next `{char}` on the line
- `F{char}` - move to the previous `{char}` on the line
- `t{char}` - move to just before the next `{char}` (till)
- `T{char}` - move to just after the previous `{char}` (till)
- `Count-f` - jump to the `Count`th occurrence

## Incremental search

- `/` - search forward
  - `n` - next match
  - `N` - previous match
- `?` - search backward

See [search-and-replace.md](search-and-replace.md) for case sensitivity, regular expressions and project-wide search.
