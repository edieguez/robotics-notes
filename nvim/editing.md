# Editing, folds & text objects

## Basic editing

- `dd` - delete the entire line
- `cc` - change the entire line
- `.` - repeat the last change (dot repeat)

## Case manipulation

- `gU{motion}` - uppercase
- `gUU` - uppercase the entire line
- `gu{motion}` - lowercase
- `guu` - lowercase the entire line

## Surround (mini.surround)

Enabled through LazyExtras `coding.mini-surround`.

- `gsa{motion}{char}` - add surrounding `{char}` to the motion, e.g. `gsaiw"` wraps a word in quotes
- `gsat` - add an HTML/XML tag around the motion, e.g. `gsaiw` then `t`
- `gsd{char}` - delete the surrounding `{char}`
- `gsr{old}{new}` - replace the surrounding `{old}` with `{new}`

> [!NOTE]
> The `gsa` prefix comes from the LazyVim mini.surround config (`add = "gsa"`). Other keys are the mini.surround defaults.

## Text objects (mini.ai)

Text objects work with operators like `d`, `c`, `y`, `v`:

- `i` - inner (excluding delimiters), `a` - around (including delimiters)
- `ciw` / `daw` - change / delete inner / around word
- `ci(` / `da"` - change inside parentheses / delete a quoted string including the quotes
- `vap` - select a paragraph

## Folds

- `zc` - close fold
- `zo` - open fold
- `za` - toggle fold
- `zR` - open all folds
- `zM` - close all folds
- `zO` - open the fold under the cursor and all nested folds recursively
- `zC` - close the fold under the cursor and all nested folds recursively

## Comments

- `gcc` - toggle comment on the current line
- `gc{motion}` - toggle comment on the motion (e.g. `gcap` for a paragraph)
- Visual `gc` - toggle comment on the selection
