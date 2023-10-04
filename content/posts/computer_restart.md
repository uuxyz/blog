---
title: computer restart
date: 2023-01-25
---
Oh, it's you. Welcome, welcome! Let me guess why you're here. What? You've managed to wreck your computer again? Lost all your data? But that's not surprising, it's quite in line with your personality, isn't it?

Even though everything needs a fresh start sometimes, life goes on, so let's fix it all! First things first, let's install a new system, don't waste time on those pointless questions. Trust me, just install Manjaro! Do you really need the freedom of Debian and Arch Linux? What have LFS and Gentoo brought you besides trouble? BSD, Unix, Hurd, or even LispOS? Don't even think about them until you're proficient enough.

After installing Manjaro, remember to leave some space for Windows. You'll definitely need the most widely used operating system in the world. Assuming you have 1TB or more of storage space, allocate 256GB to each system, and the rest can be used for file storage.

You can use `visudo` to edit the `/etc/sudoers` file. Insert the following line at the appropriate location, replacing 'u' with your own username:

```bash
u ALL=(ALL:ALL) ALL
```

If you're in an area where you're still using the old dial-up, then the following line of command may be useful.

```bash
nmcli con edit type pppoe con-name "pppoe"
```

Perhaps you've noticed that the time on Windows and Linux is always off, then it's definitely Windows' fault. Try running this piece of code:
```cmd
Reg add HKLM\SYSTEM\CurrentControlSet\Control\TimeZoneInformation /v RealTimeIsUniversal /t REG_DWORD /d 1
```

Once you've sorted out the system installation, it's time to relax online. Let's open Firefox and log into your Mozilla account. Passwords and bookmarks should sync automatically. Now it's time to access Google. Oops, it's blocked, but that's okay, where there's a will, there's a way.

Remember to update Manjaro's mirrors:

```bash
sudo pacman-mirrors -i -c China -m rank
sudo pacman -Syyu
```

Install pip and accelerate pip downloads with the following line of code:

```bash
python -m pip config set global.index-url https://mirrors.aliyun.com/pypi/simple
```

Note: This information may change rapidly over time!

First, let's download a fantastic piece of software: [v2ray](https://github.com/v2fly/v2ray-core/releases/download/v4.31.0/v2ray-linux-64.zip) .
Next, let's download its graphical interface: [v2rayA](https://github.com/v2rayA/v2rayA/releases/download/v2.2.4/v2raya_linux_x64_2.2.4) .
But where can we get some [free proxy nodes](https://ghproxy.com/https://raw.githubusercontent.com/freefq/free/master/v2) ?
If you only want to access blocked websites through a proxy, this list can be very helpful: [gfwlist.txt](https://ghproxy.com/https://raw.githubusercontent.com/gfwlist/gfwlist/master/gfwlist.txt)
Now you should know what to do!

After enjoying a smooth internet experience, it's time to ditch the ugly bash shell. Just go for oh-my-zsh with the robbyrussell theme; no need for more tinkering.

If you wish to input Chinese, please install the Rime input method and add `LC_CTYPE="zh_CN.UTF-8"` to `/etc/environment`.

And now it's time to configure your text editor, Emacs.
Your own configuration? Don't kid yourself. You should unashamedly borrow Purcell's configuration, well, I mean, learn from it; it's almost the same thing.

```bash
git clone https://github.com/purcell/emacs.d.git ~/.emacs.d
```

Don't forget to update it from time to time:

```bash
git pull
```

Next, let's go over the essential software that you just can't live without:

First, in the realm of calculation, you rely on qalc even for simple tasks like 1+1. Then there's WolframKernel, which has saved you countless times during those intense calculus sessions. And there's Matlab too, even though you've never actually used it, you can't help but think it's incredibly useful.

Moving on to management software, you must have Obsidian to keep your notes organized, or they'd turn into chaos. And you use Jellyfin to manage all those hard-earned videos and images you've collected.

Finally, in the realm of programming, you definitely need Python. And let's not forget about GCC, and Guile Scheme is also a must-have.

Now, let me list some more software that might bring back many memories. Do you recall the times when you used FFmpeg to edit videos? How about those moments spent with TexLive writing research papers? VLC and MPV were your companions for countless nights of dull solitude, playing numerous videos. Yay, on the other hand, helped you install so many applications. You were initially impressed by OnlyOffice's elegant interface. You got used to opening files with Kate, regardless of their size. You haven't used Docker yet, but one day, you might just fall in love with it.

Why has your life been so bleak that most of your time has been occupied by these seemingly meaningless tools? Perhaps you should consider finding a boyfriend or girlfriend—my apologies, you don't even have friends. But even so, even so, I hope that everyone can drop their masks and find love.