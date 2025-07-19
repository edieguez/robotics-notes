# GRUB installation guide

> This guide is also helpful for fixing a broken GRUB installation

## Prerequisites

- Live USB with a Linux distribution (e.g., Ubuntu, Arch Linux). It is better if the live USB is of the same distribution as the installed system

## Identify the installed system

Run the following command to identify the `root` and `EFI` partitions

```bash
lsblk -f
```

It will output something like this

```shell
NAME        FSTYPE FSVER LABEL    UUID                                 FSAVAIL FSUSE% MOUNTPOINTS
nvme0n1                                                                               
├─nvme0n1p1 vfat   FAT32 NO_LABEL AE69-8C73                             272.8M     9% /boot/efi
└─nvme0n1p2 ext4   1.0            f5b8fb51-51d2-4f2b-8238-3632403033d4  822.4G     5% /
```

The `nvme0n1p1` is the `EFI` partition and `nvme0n1p2` is the `root` partition. The names may vary based on your system

## Mount the partitions

Mount the `root` partition and the `EFI` partition. Replace `/dev/nvme0n1p2` and `/dev/nvme0n1p1` with your actual partitions

```bash
sudo mount /dev/nvme0n1p2 /mnt
sudo mount /dev/nvme0n1p1 /mnt/boot/efi
```

## Bind mount necessary directories

> This step may not be necessary for all distributions

```bash
sudo mount --bind /dev /mnt/dev
sudo mount --bind /proc /mnt/proc
sudo mount --bind /sys /mnt/sys
```

## Chroot into the installed system

```bash
sudo chroot /mnt

# If your are using Arch Linux
arch-chroot /mnt

# If you are using Manjaro
manjaro-chroot /mnt
```

## Install GRUB

```bash
# Short version
grub-install

# If that does not work, try the full version
grub-install --target=x86_64-efi --efi-directory=/boot/efi --bootloader-id=GRUB --recheck
```

## Update GRUB configuration

```bash
grub-mkconfig -o /boot/grub/grub.cfg
```

Exit the chroot environment with `exit` or `Ctrl+D`

## Unmount the partitions

```bash
sudo umount -R /mnt
```

## Reboot the system

> Make sure to remove the live USB before booting again

```bash
sudo reboot
```

## Change boot order (optional)

> All these commands should be run in the chroot environment

Sometimes **GRUB may not boot because Windows is set as the default boot option**. Use this command to check the current boot order

```bash
efibootmgr
```

It will output something like this

```shell
BootCurrent: 0001
Timeout: 5 seconds
BootOrder: 0001,0000,0002
Boot0000* manjaro       HD(1,GPT,a9d27b7c-f592-a545-9387-488ef2bbb3ba,0x1000,0x96000)/\EFI\MANJARO\GRUBX64.EFI
Boot0001* Windows Boot Manager  HD(1,GPT,a9d27b7c-f592-a545-9387-488ef2bbb3ba,0x1000,0x96000)/\EFI\MICROSOFT\BOOT\BOOTMGFW.EFI0000424f
Boot0002* Hard Drive    BBS(HD,,0x0)0000474f00004e4fad0000000100000073004b0049004e004700530054004f004e00200053004e005600530031003000300030004700420000000501090002000000007fff040002010c00d041030a0000000001010600010101010600000003171000010000000026b7684c0e0ea57fff040001043600ef47642dc93ba041ac194d51d01b4ce6350030003000320036004200370036003800340043003000450030004500410000007fff04000000424f
```

You can change the boot order in the BIOS/UEFI settings or use the following command to set GRUB as the default bootloader

```bash
sudo efibootmgr -o 0000,0001,0002
```

If you want to remove the Windows Boot Manager entry, you can use the following command

```bash
sudo efibootmgr -b 0001 -B
```
