# NeoVim (LazyVim) Keybindings

## Modes

- `i` - enter Insert mode - one character before the cursor
- `I` - enter Insert mode - at the beginning of the line
- `a` - enter Insert mode - one character after the cursor
- `A` - enter Insert mode - at the end of the line
- `o` - enter Insert mode one line bellow
  - When in Visual mode, it switches the selection to the other side
- `O` - enter Insert mode one line above
- `gi` - go to the last Insert place
- `v` - enter Visual mode
- `V` - select current line in Visual mode
- `Control-v` - Visual block mode
- `gv` - repeat last Visual selection
- `Shift-:` - enter Command mode
- `Control-y` - 'yes' in Command mode
- `s` - enter Flash mode (requires plugin)
- `n` - near navigation (Flash mode)

## Motion & navigation

- `$` - move to the end of the current line
- `0` - go to the beginning of the line
- `_` - go to the first printable character is the line
- `g_` - go to the last non-blank character
- `w` - move by word
- `W` - move by word (whitespace mode)
- `e` - move to the end of the current word
- `ge` - move to the end of the previous word
- `(` - move to the previous sentence
- `)` - move to the next sentence
- `%` - move to the matching bracket
- `g` - if used as an object, it represents the whole file. E.g. `gwag`
- `gg` - go to the beginning of the file
- `G` - go to the end of the file
- `Count-G` - go to the `Count` line

### Jumps

- `Control-o` - jump backward in history
- `Control-i` - jump forward in history

### Scrolling

- `Control-d` - scroll down (half window)
- `Control-u` - scroll up (half window)
- `Control-f` - scroll forward (one window)
- `Control-b` - scroll backwards (one window)
- `Control-y` - scroll up (one line)
- `Control-e` - scroll down (one line)

#### z commands

- `zt` - move cursor to the top
- `zb` - move cursor to the bottom
- `zz` - move cursor to the middle

## Search & Find mode

To use this mode you need to press `f`. The screen will dime and you can start looking for characters. The same can be
done backwards by using the `F` key. `Count-f` allows you to jump `Count` times forward/backward.

### Til mode

It is almost the same as Find mode. This mode jumps *just before* the character your are looking for

### Incremental search

- `/` - incremental search (forward)
  - `n` - next match
  - `N` - previous match
- `?` - incremental search (backwards)

## Editing

- `dd` - delete the entire line
- `cc` - change the entire line
- `.` - dot repeat
- `gsat` - surround with tag

### Case manipulation

- `gU` - UPPERCASE
- `gUU` - UPPERCASE ON THE ENTIRE LINE
- `gu` - lowercase
- `guu` - lowercase on the entire line

## LSP & language features

- `gd` - go definition
- `gr` - go references
- `K` - show context specific help (hover-like menu in IDEs)
- `Space-cr` - rename symbol
- `Space-cs` - show symbols tree
- `Space-ss` - search symbols (current file)
- `Space-sS` - search symbols (global search)
- `Space-x` - show diagnostics in the current file
- `Space-X` - show diagnostics in the current working directory
- `[[` - go to previous variable reference
- `]]` - go to next variable reference

### LSP objects

> The uppercase variants also exist, they will jump to the end of the object, not outside. These objects need to be
> combined with `[` or `]`

- `c` - class
- `f` - function
- `m` - method
- `i` - indentation (for languages like Python)
- `h` - Git hunks - blocks of code that have been modified/added
- `q` - quotes
- `b` - brackets
- `o` - language objects like blocks, loops and conditionals
- `t` - tag. For languages like HTML or XML

### Diagnostics objects

> Combine with `[` or `]`, e.g. `[t` / `]t` for the previous/next TODO or FIXME comment

- `d` - (general diagnostics)
- `e` - errors
- `w` - warnings
- `s` - spell
- `t` - TODO and FIXME comments

## Registers

NVIM has multiple registers. You can think about that as multiple *clipboards*. Most of them are maintain automatically.
To access the **Registers**, hit `"`. A list of the available registers will show up. From there, you can select the one
you need.

- A more friendly way to access the Registers is to use `Space-s"`
- To access the Registers in Insert mode, use `Control-r`
- `p` - paste when in Normal mode
- These are the registers for the common UNIX-like systems
  - `+` - default clipboard
  - `*` - selection clipboard (usually you can paste from this clipboard by using middle click)
- `_` - *Black hole* register. Anything send here will not be saved
- `0` - *last-yanked register* - it stays the same even if you delete text. It does not get replaced by other operation
than yank
- `.` *last inserted text* - text entered during last Insert mode
- `%` - *current file name* register - stores the name of the current file

### yanky.nvim

1. You can install this plugin using `LazyExtras`
2. `Space-p` - show clipboard history
3. `[-y` - after pasting, go back in yank history
4. `]-y` - after pasting, go next in yank history
5. `[p` - paste one line above
6. `]p` - paste one line below
7. `>p` paste and add indentation, one line below
8. `<p` paste and remove indentation, one line below
9. `>P` - paste and add indentation, one line above
10. `<P` - paste and remove indentation, one line above

## Buffer, window & tab management

> [!NOTE] The hierarchy goes like this Tab > window > buffer > file

- `tab` - fullscreen layout. Only one is visible at time. It is a *window* in other code editors
- `window` - also known as *pane* or *split*. It is an area within a split to show a *buffer*
- `buffer` - it is the presentation within VIM of a open file. It lives inside a split. You can view the same buffer
inside multiple splits at the same time. Since the buffer represents the same file, when you modify the file in one
buffer, the change can be seen in other splits as well
- `fold` - collapse a code block when its content is not relevant for the task at hand
- `file` - a file that exists in disk. **Each buffer can contain one file at most**

### General shortcuts

- `Space-backtick` - move to the previous focused buffer
- `[b` - move to the buffer at the left
- `]b` - move to the buffer at the right
- `Space-wh` - move to the window at the left
- `Space-wl` - move to the window at the right
- `Space-ws` - horizontal window split
- `Space-wv` - vertical window split
- `Space-wo` - close all windows except the current one
- `Space-wT` - close current buffer and open it in a new tab
- `Space-,` - open picker (currently open buffers)

### Opening files from pickers

> [!NOTE]
> This shortcuts have to be executed on a picker

- `Control-v` - open file in a vertical split
- `Control-s` - open file in a horizontal split
- `Control-x` - close the file buffer

### Buffer management shortcuts

- `Space-bD` - close buffer and the split containing it
- `Space-bl` - close all buffers on the left
- `Space-br` - close all buffers on the right
- `Space-bo` - close all buffers except the current one
- `Space-bp` - pin current buffer
- `Space-bP` - close all the non-pinned buffers

### Hydra mode

Allows to run multiple *window* commands at once. Useful when you want to setup a layout. Activate with
`Space-w-Space-v`

```vim
# Generate three vertical splits and a horizontal split
Space-w-Space-vvvs
```

## Code folding

- `zc` - colapse fold
- `zo` - open fold
- `za` - toggle fold
- `zR` - open all folds
- `z0` - open all folds recursively. To be used on a fold with nested folds

## Sessions

- `Space-qq` - save session and close LazyVim
- `Space-qs` - restore session. Depends of the current directory
- `Space-qS` - restore session. Shows a picker to select the saved session
- `Space-qd` - close LazyVim without saving the current session

## Pickers

- `Alt-s` - while using a picker, it will enter in Find mode

### Scrolling

- `Control-d|u` - scroll down/up in the results window
- `Control-f|b` - scroll down/up in the preview window

## Config

- `Space-fc` - find config - open the configuration directory
- `Space-l` - show Lazy.nvim plugin manager

## Plugins

- mini.files - included in LazyExtras
- nvim.spider - third-party
- mini.surround - plugin to operate on bracket-like characters
- yanky.nvim - better registers management
