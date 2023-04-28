# [ntfs-3g](https://help.ubuntu.com/community/MountingWindowsPartitions)

Mount NTFS filesystems with read-write support

## Using ntfs-3g command

```bash
ntfs-3g /dev/sda1 /run/media/Windows
```

## Using `fstab`

Get the UUID of the partition

```bash
blkid # List all partitions
blkid /dev/sda1 # Get UUID of /dev/sda1
```

Use the UUID in `/etc/fstab`

```bash
UUID=7C24DA5B24DA184A  /run/media/Windows  ntfs-3g  defaults,windows_names  0 0
```

> You can also use the block device name (e.g. `/dev/sda1`) instead of the UUID
