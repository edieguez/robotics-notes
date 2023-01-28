# Useful packages

## QT file picker

Force some applications to use the QT file picker instead of GTK

- xdg-desktop-portal
- xdg-desktop-portal-kde

Some programs will recognize this packages automatically, others not. For those, you can set the following environment variable in a file within the `~/.kde/env` directory

```bash
export GTK_USE_PORTAL=1
```
