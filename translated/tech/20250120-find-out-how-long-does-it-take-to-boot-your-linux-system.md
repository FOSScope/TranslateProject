---
title: 了解你的 Linux 系统启动需要多长时间
date: {{release_date}}
abbrlink: 
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - 技术
tags: 
  - {{tags}}
authorInfo: |
  via: https://itsfoss.com/check-boot-time-linux/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesnied](https://github.com/excniesnied)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

这里有一个小技巧，可以让你了解自己的 Linux 系统启动需要多长时间，以及背后的原因。

<!-- more -->

当你启动系统时，你会等待制造商的标志出现，屏幕上可能会显示一些消息（以不安全模式启动），接着是 Grub 界面、操作系统加载界面，最后是登录界面。

你有没有查看过整个过程花了多长时间呢？也许没有。除非你真的需要知道，否则你不会在意启动时间的细节。

但如果你好奇自己的 Linux 系统启动需要多长时间呢？使用秒表计时是一种方法，但在 Linux 中，你有更好、更简单的方法来了解系统的启动时间。

## 使用 systemd-analyze 检查 Linux 系统的启动时间

{% image https://itsfoss.com/content/images/wordpress/2019/08/linux-boot-time-800x450.jpg '' %}

不管你喜不喜欢，大多数流行的 Linux 发行版都在运行 systemd。systemd 有许多管理 Linux 系统的实用工具，其中之一就是 systemd-analyze。

systemd-analyze 命令会详细显示上次启动时运行了哪些服务，以及每个服务花费的时间。

如果你在终端中运行以下命令：

```
systemd-analyze
```

你将得到总的启动时间，以及固件、引导加载程序、内核和用户空间各自花费的时间：
```
Startup finished in 7.275s (firmware) + 13.136s (loader) + 2.803s (kernel) + 12.488s (userspace) = 35.704s

graphical.target reached after 12.408s in userspace
```
从上面的输出可以看出，我的系统大约花了 35 秒才进入可以输入密码的界面。我使用的是戴尔 XPS Ubuntu 版，它配备了固态硬盘，但启动仍然需要这么长时间。

不太令人满意，对吧？你不妨分享一下你系统的启动时间，咱们来比一比。

你可以使用以下命令将启动时间进一步细分到每个单元：
    systemd-analyze blame

这将产生大量输出，所有服务将按照花费时间从长到短的顺序列出。
```
          7.347s plymouth-quit-wait.service
          6.198s NetworkManager-wait-online.service
          3.602s plymouth-start.service
          3.271s plymouth-read-write.service
          2.120s apparmor.service
          1.503s [email protected]
          1.213s motd-news.service
           908ms snapd.service
           861ms keyboard-setup.service
           739ms fwupd.service
           702ms bolt.service
           672ms dev-nvme0n1p3.device
           608ms systemd-backlight@backlight:intel_backlight.service
           539ms snap-core-7270.mount
           504ms snap-midori-451.mount
           463ms snap-screencloud-1.mount
           446ms snapd.seeded.service
           440ms snap-gtk\x2dcommon\x2dthemes-1313.mount
           420ms snap-core18-1066.mount
           416ms snap-scrcpy-133.mount
           412ms snap-gnome\x2dcharacters-296.mount
```
{% note 💡 '请记住，这些服务是并行运行的。并不是说 plymouth-quit-wait.service 运行 7 秒后，NetworkManager 再运行 6 秒。它们是相互并行运行的。' color:green %}

## 额外贴士：缩短启动时间

从输出结果可以看出，网络管理器和 Plymouth 都占用了大量的启动时间。

Plymouth 负责在 Ubuntu 和其他发行版的登录界面之前显示启动动画。网络管理器负责网络连接，你可以将其关闭以加快启动时间。别担心，登录后，你的 Wi-Fi 仍会正常工作。

```
sudo systemctl disable NetworkManager-wait-online.service
```

如果你想恢复更改，可以使用以下命令：

```
sudo systemctl enable NetworkManager-wait-online.service
```

{% note 🚧 '现在，请不要在不了解服务用途的情况下自行禁用各种服务，这可能会产生严重后果。' color:red %}

同样，你也可以使用 systemd 来调查你的 Linux 系统关机时间过长的原因。

**_既然你已经知道如何检查 Linux 系统的启动时间了，何不在评论区分享一下你系统的启动时间呢？_**