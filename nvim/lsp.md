# LSP, diagnostics & Treesitter

> [!IMPORTANT]
> All of these features depend on the `lang.*` extras from LazyExtras and on the `mason` plugin.

## Mason & messages

- `Space-cm` - open the Mason menu to install, update and remove language servers, formatters and linters
- `Space-cl` - LSP info / configured servers for the current buffer (`Snacks.picker.lsp_config`)
- `Space-snl` - Noice: show the last message
- `Space-sna` - Noice: show all messages in the current session

## LSP actions

- `gd` - go to definition
- `gr` - go to references
- `K` - hover: contextual help for the symbol under the cursor
- `Space-cr` - rename the symbol
- `Space-cs` - show the document symbols tree
- `Space-ss` - search symbols in the current file
- `Space-sS` - search symbols in the whole workspace
- `Space-ca` - code actions popup
- `Space-cf` - format the buffer
- `Space-co` - organize imports > [!WARNING] verify (depends on the language extra)
- `Space-sR` - resume the previous picker search
- `[[` / `]]` - go to the previous / next reference of the variable under the cursor

## Diagnostics

Navigate diagnostics with `[` and `]`. The following objects are available:

1. `d` - general diagnostics
2. `w` - warnings
3. `e` - errors
4. `s` - spelling
5. `t` - TODO, FIX and FIXME comments

Examples: `[d` / `]d` for the previous / next diagnostic, `]e` for the next error, `[t` / `]t` for the previous / next TODO.

### Diagnostics lists (Trouble)

- `Space-xx` - workspace diagnostics window
- `Space-xX` - diagnostics for the current buffer only
- `Control-q` in a picker - send the results to the quickfix list
- `Alt-t` - Trouble window > [!WARNING] verify. On macOS, `Alt` needs the terminal to send Option as Meta, otherwise the key does nothing

## Treesitter textobject moves

These are provided by `nvim-treesitter-textobjects` and combine with `[` (previous) or `]` (next).

- `]f` / `[f` - next / previous function start (LazyVim default)
- `]c` / `[c` - next / previous class start (LazyVim default)
- `]a` / `[a` - next / previous parameter (LazyVim default)
- `]m` / `[m` - next / previous method > [!WARNING] verify (in the plugin README, not in LazyVim defaults)
- `]o` / `[o` - next / previous loop, conditional or block > [!WARNING] verify (same as above)
- `]F` / `[F`, `]C` / `[C` - jump to the **end** of the function / class > [!WARNING] verify

> [!NOTE]
> `]h` / `[h` jump between git hunks. They come from `gitsigns.nvim`, not from Treesitter.

## Plugins

1. `nvim-treesitter-context` - shows the enclosing code context at the top of the window, similar to freezing a row in Excel
   - Enabled through LazyExtras `ui.treesitter-context`
   - Toggle it with `Space-ut`
2. TODO: investigate a better way to manage *marks* or *bookmarks*
