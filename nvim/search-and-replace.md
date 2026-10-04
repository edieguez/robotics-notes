# Search & replace

## `/` search

> [!NOTE] `/` works in Normal mode.

Press `/` and start typing what you want to find. The search only applies to the current file.

Once the search is done, use `n` to jump to the next result and `N` to go to the previous one.

If what you are looking for is before the cursor, use `?` to search backward.

### Case sensitivity

With LazyVim, searches are case insensitive by default, because `ignorecase` and `smartcase` are on. If you type an UPPERCASE letter, the search becomes case sensitive.

Vanilla Vim is case sensitive by default. Use `\c` to force case-insensitive search, or `\C` to force case-sensitive search for the exact case you typed.

### Regular expressions

> [!TIP]
> `:help magic` has the full documentation for Vim regular expressions.

Vim regular expressions are not PCRE. They predate that *standard*.

Regular expression search is on by default ("magic" mode). `\V` (very nomagic) makes most characters literal, so you can search for text that contains special characters.

## Searching in the project

Press `Space-/` to search the whole project. It opens a picker. The search runs on `ripgrep`, so it must be installed for this to work.

## Substitute command (`:s`)

Full form: `:s/pattern/replacement/`

1. `:s/pattern/` starts the substitute and the second `/` separates the pattern from the replacement.
2. The closing `/` is optional when there is no flag.

### Substitute ranges

> [!TIP]
> `:help range` has the full documentation for ranges.

1. `.` - the current line. It is the default, so you can omit it.
2. `%` - the whole file.
3. `n` - only line *n*.
4. `n,m` - from line *n* to line *m*.
5. `/pattern/` - the next line that matches *pattern*, e.g. `:.,/end/s/a/b/` runs from here to the next `end` line.

### Flags

1. `g` - global. Replace all the occurrences on a line, not only the first one.
2. `i` - ignore case for this command > [!WARNING] verify (on by default only because of LazyVim's `ignorecase`).
3. `I` - match case exactly.
4. `c` - ask for confirmation before every replacement.

## Project-wide search & replace

LazyVim ships with [grug-far](https://github.com/MagicDuck/grug-far.nvim). Press `Space-sr` to open it.

Example of code you could search and replace in:

```python
class FizzBuzz:
    fizzBuzz: str

    def fizz_buzz(self):
        self.fizzBuzz = "FIZZ_BUZZ"
```

## Working with a Visual range

If you select a range in Visual mode, press `:` to get `:'<,'>`. Then:

- `:'<,'>w path/to/new_file` - save only the selected lines into a new file
- `:'<,'>s/pattern/replacement/g` - substitute only inside the selection

## Plugins

1. `text-case.nvim` - text transformations like Title Case, CamelCase, snake_case and so on. It also provides the `:Subs` command.
2. `nvim-rip-substitute` - a friendlier search-and-replace dialog. **Not installed** in this setup, so it is optional.
