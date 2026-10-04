# NeoVim (LazyVim) notes

Personal notes about Neovim with [LazyVim](https://www.lazyvim.org/). Keybindings are grouped by topic.

## Legend

- `Space` - the leader key
- `Control` - the Ctrl key (e.g. `Control-o` is `Ctrl` + `o`)
- `Alt` - the Option key on macOS. It only works if the terminal sends Option as Meta

## Topics

- [Motions, modes & search](./motions.md) - modes, motions, jumps, scrolling, `z` commands, find and incremental search
- [Editing, folds & text objects](./editing.md) - editing, case, surround, folds, comments, text objects
- [Registers & yanky](./registers.md) - registers, clipboard and yank history
- [Windows, buffers & tabs](./windows-buffers.md) - tabs, windows, buffers, pickers and splits
- [LSP, diagnostics & Treesitter](./lsp.md) - Mason, LSP actions, diagnostics, Treesitter textobject moves
- [Sessions, config & search](./sessions-config.md) - sessions, config files, plugin manager, common finders
- [Search & replace](./search-and-replace.md) - `/` search, regular expressions, `:s`, project-wide replace
- [Ex commands](./ex-commands.md) - `:global` and `:normal`, command history

## Plugins

- `flash.nvim` - jump by label
- `mini.ai` - extra text objects
- `mini.files` - file explorer (LazyExtras)
- `mini.surround` - operate on surrounding characters (LazyExtras `coding.mini-surround`)
- `nvim-treesitter-context` - sticky code context at the top of the window (LazyExtras `ui.treesitter-context`)
- `nvim-treesitter-textobjects` - move and select by syntax node
- `nvim.spider` - third-party, smarter `w` / `e` / `b` motions
- `persistence.nvim` - sessions (bundled with LazyVim)
- `snacks.nvim` - pickers (files, buffers, grep, symbols)
- `trouble.nvim` - diagnostics and lists window
- `yanky.nvim` - better registers and yank history (LazyExtras `coding.yanky`)
