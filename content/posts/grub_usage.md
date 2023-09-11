---
title: grub usage
date: 2022-03-29
---
When configuring multiple operating systems, inadvertent actions often result in the loss of boot entries, rendering us unable to access our systems properly. Therefore, learning how to correctly configure the GRUB bootloader is highly valuable.

In GRUB's rescue mode, only a few commands like cmdpath, prefix, root, insmod, ls, set, unset, and others are available.

To begin, you should use insmod to load the necessary modules, such as:

```sh
insmod gpt
insmod ntfs
insmod chain
set root=(hd0,msdos1)  # Modify as per your system configuration
```

If you are using a Linux system, you should load the kernel like this:

```sh
linux /vmlinux root=/dev/sda1
```

Then:

```sh
initrd /initrd
```

Finally, start the system:

`boot`

This set of commands is essential for booting a Linux system properly from GRUB's rescue mode.

If you are using a Windows system, use chainloader to load the system:

`chainloader +1`

Then proceed to start the system:

`boot`

Properly configuring GRUB in situations like this can be instrumental in recovering from boot-related issues when managing multiple operating systems.