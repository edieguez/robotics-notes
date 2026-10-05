# Miscellaneous commands

## Filtering current file content through external programs

`%!jq` - format the current (`json`) file using `jq`

## Spell check

1. `Space-us` - toggle spell checking
2. `z=` - show suggestions for the current misspelled word
3. `zg` - add the current word to the personal dictionary
4. `[s` and `]s` - navigate to the previous/next misspelled word

## Normal mode in Insert mode

While in Insert mode you can press `Control-o` to enter in Insert mode. Once you enter a command, VIM will get back to
insert mode.

## VIM calculator

1. While in Insert mode, press `Control-r`, the `=`
2. After performing a calculation, the result will be inserted in the current buffer

## Paste in Insert mode

While in Insert mode, press `Control-a` to paster from the clipboard.
