# [The pernicious USB-stick stall problem](https://lwn.net/Articles/572911)

When copying a large file to a USB stick, the file is written to the cache and the copy completes quickly. However, the file is not actually on the USB stick yet. If you remove the USB stick before the file is actually written, the file is lost.

The *solution* is to use the `sync` command to flush the cache to the USB stick before removing it.

Another alternative is to increase the `vm.dirty_ratio` and `vm.dirty_background_ratio` values to force the kernel to flush the cache more often. That solution was suggested by [Linus Torvalds himself](https://lwn.net/Articles/572921). **These changes are not persistent across reboots**

```bash
echo $((16*1024*1024)) | sudo tee /proc/sys/vm/dirty_background_bytes
echo $((48*1024*1024)) | sudo tee /proc/sys/vm/dirty_bytes
```

Alternatively, you can use the `sysctl` command to set the values

```bash
# Set the dirty ratio to 40% and the dirty background ratio to 20%
sudo sysctl -w vm.dirty_ratio=40
sudo sysctl -w vm.dirty_background_ratio=20
```

To make them persistent across reboots, add the following lines to `/etc/sysctl.conf` or `/etc/sysctl.d/99-sysctl.conf` (or any other file in `/etc/sysctl.d/` in [newer distributions](https://archlinux.org/news/deprecation-of-etcsysctlconf/))

```bash
vm.dirty_ratio=40
vm.dirty_background_ratio=20
```

## References

- [Blog-D without nonsense](https://dannyda.com/2022/05/14/how-to-check-show-set-change-modify-current-disk-caching-values-vm-dirty_ratio-vm-dirty_background_ratio-etc-on-linux-debian-ubuntu-kali-linux-fedora-redhat-rocky-linux-etc/)
