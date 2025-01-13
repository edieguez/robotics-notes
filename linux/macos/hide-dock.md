# Hiding MacOS dock

To hide the MacOS dock, you can use the following command. With this the dock will appear after 1 hour

```bash
defaults write com.apple.dock autohide-delay -float 3600; killall Dock
```

To show the dock again, you can use the following command

```bash
defaults delete com.apple.dock autohide-delay; killall Dock
```

## Reference

- [Is there a way to completely disable Dock?](https://apple.stackexchange.com/questions/59556/is-there-a-way-to-completely-disable-dock)
