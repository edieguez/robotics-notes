# Windows, buffers & tabs

> [!NOTE] The hierarchy goes like this: Tab > window > buffer > file

- `tab` - a full-screen layout of windows. Only one tab is visible at a time. It is closer to a workspace or virtual desktop than to a window in other editors
- `window` - also known as *pane* or *split*. It is an area inside a tab that shows a *buffer*
- `buffer` - the in-memory representation of an open file. It lives inside a window. The same buffer can be shown in several windows, so a change in one is visible in the others
- `file` - a file on disk. **Each buffer holds one file at most**
- `fold` - collapse a block of code that is not relevant for the task at hand (see [editing.md](editing.md#folds))

## Window shortcuts

- `Control-h` - move to the window on the left
- `Control-j` - move to the window below
- `Control-k` - move to the window above
- `Control-l` - move to the window on the right
- `Space-ws` - horizontal split
- `Space-wv` - vertical split
- `Space-wo` - close all windows except the current one
- `Space-wT` - move the current window to a new tab > [!WARNING] verify (may not close the buffer)
- `Space-` `` ` `` - switch to the previously focused buffer

## Buffer shortcuts

- `[b` - previous buffer
- `]b` - next buffer
- `Space-,` - picker with the open buffers

### Buffer management

- `Space-bd` - delete (close) the buffer, keep the window
- `Space-bD` - delete the buffer and close its window
- `Space-bl` - close all buffers to the left
- `Space-br` - close all buffers to the right
- `Space-bo` - close all buffers except the current one
- `Space-bp` - pin / unpin the current buffer
- `Space-bP` - close all non-pinned buffers

## Pickers (snacks.nvim)

Pickers are the fuzzy finders: files, buffers, grep, symbols, etc. The following keys work **inside** a picker:

- `Control-s` - open the file in a horizontal split
- `Control-v` - open the file in a vertical split
- `Control-q` - send the results to the quickfix list > [!WARNING] verify
- `Alt-s` - switch to Find mode in the picker > [!WARNING] verify
- `Control-d` / `Control-u` - scroll the results window down / up
- `Control-f` / `Control-b` - scroll the preview window down / up

## Hydra mode

Runs several window commands in a row, which is useful to set up a layout. Activate it with `Space-w-Space-v` > [!WARNING] verify (check which hydra plugin provides this and its exact trigger)

Example, which should create three vertical splits and a horizontal one:

```vim
Space-w-Space-vvvs
```
