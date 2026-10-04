# Ex commands: `:global` & `:normal`

Ex commands run from Command mode (`Shift-:`). Two of them are useful together: `:global` runs a command on every matching line, and `:normal` plays Normal mode keys on each line.

## `:global` (`:g`)

It runs a command on **every** line that matches a pattern. It can be combined with [`:normal`](#normal-norm).

Basic syntax (both forms are equivalent):

1. `:<range>g/pattern/command` - short form
2. `:<range>global/pattern/command` - long form

### Delete all lines matching a pattern

> `:%g/pattern/d`

- `%` - act on all the lines of the current file
- `g` - *global* command (short form)
- `pattern` - *pattern* to match
- `d` - *delete* command. It is applied on every line that matches *pattern*

### Substitute on every matching line

> `:%g/^f/s/ba[rt]/glib`

- `%` - act on all the lines of the current file
- `g` - *global* command (short form)
- `^f` - *pattern* - matches all the lines that start with *f*
- `s` - *substitute* command
  - `ba[rt]` - search pattern
  - `glib` - replacement

### Negating `:global`

Use `:g!` or `:v` to act on the lines that do **not** match a pattern. Both are equivalent:

> `:v/pattern/d`
> `:g!/pattern/d`

This is useful to clean files with unwanted data, like log files, or to remove malformed rows.

> [!NOTE] `g/re/p` stands for *Global / Regular Expression / Print*. It prints every matching line, which is handy to preview what a `:g` will act on.

## `:normal` (`:norm`)

It lets you run Normal mode keys on each line of a range, without pressing them one by one.

### Escaping keys

You cannot press `Esc` while typing the command, so insert the escape sequence instead: press `Control-v` followed by `Esc`. It inserts `^[`.

### Ranges

- `:%norm Atext` - append `text` to every line of the file
- `:'<,'>norm Atext` - the same, but only on the lines of the current Visual selection (Vim fills in `'<,'>` when you press `:` in Visual mode)

### Combining with `:global`

> `:g/^TODO/norm I-`

It inserts `-` at the start of every line that begins with `TODO`.

## Editing command history

1. In Normal mode, press `Control-f`, or
2. In Normal mode, press `q:`

Either opens a window with the commands you ran in the current session. It is a buffer, so you can edit a previous command. Press `Enter` to run the (edited) command again.

The window shows the history with the most recent command at the bottom. Use `Control-u` to scroll up.
