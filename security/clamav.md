# [ClamAV](https://www.clamav.net/)

## Installation (Arch Linux)

```bash
sudo pacman -S clamav
# or
sudo yay -S clamav
```

## Update database

Is important to update the database before scanning

```bash
sudo freshclam
```

## [Scan](https://askubuntu.com/questions/250290/how-do-i-scan-for-viruses-with-clamav)

> `/sys` is excluded because it is a virtual filesystem and it is not possible to scan it. Doing so will result in a system crash

```bash
# Short form
clamscan -ir --exclude-dir="^/sys" --bell /

# Long form
clamscan --infected --recursive --exclude-dir="^/sys" --bell /
```
