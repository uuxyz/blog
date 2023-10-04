---
title: mount disks
date: 2023-09-15
---
```bash
sudo cryptsetup open --type luks disk.img disk
udisksctl mount -b /dev/mapper/disk
```