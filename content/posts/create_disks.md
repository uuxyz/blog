---
title: create disks
date: 2023-09-14
---
```bash
fallocate -l 4GiB disk.img
cryptsetup luksFormat --type luks disk.img
sudo cryptsetup luksOpen disk.img secretum
sudo mkfs.ext4 /dev/mapper/secretum
udisksctl mount -b /dev/mapper/secretum
sudo chown -R u:u /run/media/u/fe299871-a3b6-4506-be6c-505b8eb41bec
```