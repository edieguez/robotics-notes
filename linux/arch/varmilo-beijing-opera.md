# Apple Magic Keyboard (Linux)

Notes on getting an Apple Magic Keyboard — or an Apple-layout third-party board — to behave correctly on Linux.

## Fn key behaviour (`hid_apple` driver)

Edit `/etc/modprobe.d/hid_apple.conf`:

```text
options hid_apple fnmode=2
```

## [Varmilo Beijing Opera](https://varmilo.com/blogs/switches-1/the-new-varmilo-beijing-opera-themed-keyboard)

A themed colorway of Varmilo's **VA87M** (TKL, 87-key) / **VA108M** (full-size, 108-key) mechanical keyboards, with dye-sub PBT keycaps depicting Chinese opera masks.

### Features

| Feature | Detail |
| --- | --- |
| Layout | ANSI, TKL (VA87M) or full-size (VA108M) |
| Switches | Cherry MX (Black, Brown, Red, Blue, Clear, Silver, Silent Red/Black variants exist across the line) |
| Keycaps | Dye-sublimated PBT, doubleshot-style legends, some SKUs translucent for backlight |
| Backlight | White LED on backlit SKUs only; no backlight on non-lit SKUs |
| Connectivity | Wired, detachable USB cable (mini-USB/USB-C depending on revision); no Bluetooth/2.4G on this board |
| Rollover | Full NKRO over USB |
| Onboard memory | All Fn functions are stored on the controller; no driver/software required |
| OS modes | Switchable **Windows** and **Apple/Mac** input modes (remaps Win/Alt to Cmd/Opt and adjusts Fn-row behavior) |

### Troubleshooting

> Symptom: Caps Lock and Ctrl are swapped, the Windows key doesn't work, or Windows and Fn are swapped.

1. Hold **Fn + Esc** for ~4 seconds. The Capslock LED flashes 3 times when the reset succeeds.
2. If Fn and left Windows are already swapped, use **left Windows + Esc** instead — same 4 second hold, same 3-flash confirmation.

This is a full factory reset: see [Reset](#reset) below for exactly what it clears.

### Shortcuts

All combinations are pressed by holding **Fn** first, then the second key. Legends may vary slightly by revision/SKU — check the icons printed on your keycaps if something below doesn't respond.

#### Top row (R1) mode

| Combination | Function |
| --- | --- |
| Fn + PgUp | Set R1 (top row) to number-row output |
| Fn + PgDn | Set R1 (top row) to function-row (F1–F12) output |

Changes only what R1 sends *without* Fn held. Secondary legends on that row (media keys, etc.) are still reached by holding Fn either way.

#### Key locking & remapping

| Combination | Function | Persistent? |
| --- | --- | --- |
| Fn + Windows | Lock/unlock the Windows key | No |
| Fn + Right Ctrl | Menu key | — |
| Fn + Windows (hold ~4s, until LED flashes) | Swap Windows ↔ Fn | Yes |
| Fn + Left Ctrl (hold ~4s, until LED flashes) | Swap Ctrl ↔ Capslock | Yes |

The **lock** is a quick, non-persistent toggle to stop the Windows key firing by accident (e.g. mid-game) — press again to undo. The **swaps** are different: they're stored on the controller and survive unplugging, reboots, and OS-mode switches, until repeated or cleared by a [reset](#reset).

#### OS mode

| Combination | Function |
| --- | --- |
| Fn + W (hold ~3s) | Switch to Windows mode |
| Fn + A (hold ~3s) | Switch to Apple/Mac mode |

Changes how modifiers report themselves: Apple mode remaps Win/Alt to Cmd/Opt and adjusts the F-row default to match macOS conventions. This is the keyboard's own equivalent of the `hid_apple fnmode` setting above, done on the controller instead of the Linux driver — pick one or the other, not both.

#### Reset

| Combination | Function |
| --- | --- |
| Fn + Esc (hold ~4s, until LED flashes 3 times) | Factory reset |

Clears all persistent state: undoes the Windows/Fn swap, the Ctrl/Capslock swap, and returns OS mode to Windows. Use this whenever the keyboard is in a confusing state and you're not sure what's currently swapped.

#### Media keys

| Combination | Function |
| --- | --- |
| Fn + F7 | Previous track |
| Fn + F8 | Play / Pause |
| Fn + F9 | Next track |
| Fn + F10 | Mute |
| Fn + F11 | Volume down |
| Fn + F12 | Volume up |

One-shot signals — no persistent state involved.

#### Backlight (backlit SKUs only)

| Combination | Function |
| --- | --- |
| Fn + X | Toggle backlight on/off |
| Fn + Right Arrow | Cycle lighting mode: always-on ↔ breathing |
| Fn + Up / Down Arrow | Always-on mode: brightness up/down · Breathing mode: pulse speed up/down |

`Fn + Up/Down` is mode-dependent: the same combo adjusts brightness in always-on mode, but pulse speed once breathing mode is active.
