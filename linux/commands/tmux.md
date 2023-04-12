# TMUX (Terminal Multiplexer)

TMUX is a terminal multiplexer. It allows you to create multiple terminal sessions within a single terminal window

## References

- [tmux cheatsheet](https://tmuxcheatsheet.com)
- [gpakosz/.tmux](https://github.com/gpakosz/.tmux)

## Hierarchy

`session` > `window` > `pane`

## Commands

``` bash
tmux new-session # create new session

tmux ls # list sessions

# attach to session
tmux a
tmux attach

# kill window number 1
tmux kill-window -t 1
```

## Shortcuts

Before using shortcuts, press `Ctrl + b` to enter command mode. I'll be refering to this as `prefix`.

- `prefix + ?` list shortcuts
- `prefix + :` enter command mode

### Session

- `prefix + d` detach from session
- `prefix + s` list sessions
- `prefix + $` rename session

### Window

- `prefix + c` create new window
- `prefix + ,` rename window
- `prefix + w` list windows
- `prefix + n` next window
- `prefix + p` previous window
- `prefix + 0-9` switch to window number
- `prefix + &` kill window

### Pane

- `prefix + %` split pane vertically
- `prefix + "` split pane horizontally
- `prefix + o` switch to next pane
- `prefix + q` show pane numbers
- `prefix + {` move current pane left
- `prefix + }` move current pane right
- `prefix + x` kill current pane

### Command mode

- `set -g mouse on` enable mouse support
