# Language Server Protocol (LSP) support

> [!IMPORTANT]
> All of this features depend on the `lang.*` from `LazyExtras` and the `mason` plugin

You can access the Mason menu by hitting `Space-cm`. It will pop up a dialog where you can manage all your language
servers

- `Space-sn` - open `Noice` dialog
  - `a` - show all the messages in the current session
  - `l` - show only the last **change**
- `Space-cl` - show a picker with all the installed LSPs

## Diagnostics

You can navigate `diagnostics` using the `[` and `]` keys. While doing so, you have the following object available

1. `diagnostics`
2. `warning`
3. `error`
4. `spell`
5. `TODO`, `FIX`, `FIXME` comments

### General shortcuts

- `Space-x` - invoke the quick fix dialog
- `Space-xx` - show diagnostics window
- `Space-ca` - code actions popup
- `Space-cf` - code format
- `Space-co` - optimize imports
- `gd` - go to definition
- `gr` - go to references
- `Space-sR` - resume previous picker search
- `Alt-t` - invoke Trouble window - looks it does not work on MacOS
- `Control-q` - similar to the previous one. It dumps the results from a picker in the Quick Fix window
- `K` - show *hover* dialog (contextual help)
- `Space-ss` - list symbols
- `Space-cs` - show the Document Symbols window

## Plugins

1. `nvim-treesitter-context` - show code context in the editor. Similar to fixing a row/column in Excel
   1. It can be installed using `LazyExtras`
   2. Toggle it with `Space-ut`
2. Investigate a better way to manage *marks* or *bookmarks*
