# Apple magic keyboard

Edit `/etc/modprobe.d/hid_apple.conf`

```text
options hid_apple fnmode=2
```

## [Varmilo Beijing opera](https://en.varmilo.com/keyboardproscenium/selectproductpage?subject_name=Beijing+Opera)

**VA87/108** Caps lock and ctrl is switched, or Win key doesn’t work, or Win and FN is switched

Hold **Fn down and press ESC** about 4 seconds, if Capslock backlight can flash 3 times, it means reset succeed. If FN and left WIN swapped, hold left WIN down, and press ESC about 4 seconds, Capslock backlight will flash 3 times.

### Shortcuts

- FN + PgUp: Toggle number row for R1
- FN + PgDn: Toggle Function row for R1
- FN + Windows: Windows Lock
- FN + Windows (Hold until LED flashes): Swap Windows and Function keys
- FN + Left Ctrl (Hold unit LED flashes): Swap Ctrl and Capslock keys
