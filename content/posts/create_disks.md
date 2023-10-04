---
title: create disks
date: 2023-09-14
---
```bash
fallocate -l 4GiB disk.img
mkfs.ext4 disk.img
```