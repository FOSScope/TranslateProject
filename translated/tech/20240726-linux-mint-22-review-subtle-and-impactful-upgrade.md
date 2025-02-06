---
title: "Linux Mint 22 评测：细微却影响深远的升级"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/mint-22.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/mint-22.png
categories:
  - 翻译
  - 技术
tags: 
  - Linux Mint
  - Linux 发行版评论
authorInfo: |
  via: https://itsfoss.com/linux-mint-22

  作者：[Ankush Das](https://itsfoss.com/author/ankush/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

Linux Mint 22 来了！让我们一起看看它带来了哪些升级。

<!-- more -->

每次 Ubuntu LTS 版本发布后，大家就开始期待一些优秀衍生版的升级，其中就包括 Linux Mint。

现在，[Linux Mint 22 已经发布](https://news.itsfoss.com/linux-mint-22-release/)，它基于 [Ubuntu 24.04 LTS](https://itsfoss.com/ubuntu-24-04-lts-review/)。

*但是，你应该立即升级吗？你能期待哪些改进呢？*

我对这个发行版进行了测试，为你提供了一些细节，以帮助你做出决定。

## Linux Mint 22：有哪些新特性？

![linux mint 22 截图](https://itsfoss.com/content/images/2024/07/linux-mint-22-main.png)

虽然你可以查看发布新闻获取所有信息，但我在这里为你总结了主要的变化：

- **声音服务器切换到 Pipewire**
- **Linux 内核 6.8**
- **基于 Ubuntu 24.04**
- **默认禁用未验证的 Flatpak 应用**
- **预装 Matrix 网络应用**
- **Cinnamon 6.2 新增布局编辑器**
- **其他桌面环境升级**

和往常一样，Linux Mint 并没有进行大规模的视觉改造。所以，你将获得熟悉的体验，并在此基础上有所改进。

让我们仔细看看一些变化。

## 用户体验和桌面环境升级

![linux mint 22 屏幕截图](https://itsfoss.com/content/images/2024/07/linux-mint-22-file-manager.png)

在 Linux Mint 21.3 中，我们在文件夹图标、颜色和主题方面获得了许多有意义的用户体验升级。

不过，Linux Mint 22 专注于保持这些特性不变，并改进可用的工具，以提升用户体验。

例如，在升级到 **Cinnamon 6.2 后，新增了 Nemo 操作菜单布局编辑器**。

![linux mint nemo 操作菜单](https://itsfoss.com/content/images/2024/07/linux-mint-actions.png)

要访问此功能，你可以打开「操作」应用，然后导航到「布局」菜单，在那里你可以找到添加/删除或切换右键上下文菜单选项的功能。

还有更多实用的用户体验改进，例如：

- 添加新的启动应用时可以搜索应用程序。
- 使用鼠标中键关闭工作区。
- 屏幕锁定延迟选项为 5 - 10 秒。

## 软件管理器注重更好的安全性

![linux mint 22 软件管理器](https://itsfoss.com/content/images/2024/07/linux-mint-22-software-manager.png)

Linux Mint 软件管理器的每次更新都能提供出色的体验。

在 Linux Mint 22 中，它进行了性能改进，包括加入多线程支持以及首次在软件管理器中添加 **横幅幻灯片展示**，以展示一些流行的 Linux 应用，如上图所示。

![linux mint 22 设置中的未验证 Flatpak 应用](https://itsfoss.com/content/images/2024/07/linux-mint-software-manager-flatpak.png)

为了增强安全性，Linux Mint 团队决定默认禁用显示任何未验证的 Flatpak 应用。你可以在新的偏好设置屏幕中启用「*显示未验证的 Flatpak 应用*」来更改此设置。

并且，在启用该选项时，你会看到安全警告，它是防止任何恶意软件影响 Linux 用户的一个良好安全实践。这也应该能够鼓励 Flatpak 维护者尽可能地让他们的应用通过验证。

当然，如果你信任或了解某个 Flatpak 的非官方维护者并已经进行过研究，你可以选择安装它。所以，用户有做出选择的权利。

虽然这是一种实用的安全方法，但因此你可能无法在 Flathub 商店中找到所有类型的应用。

![已验证的 Flatpak 应用](https://itsfoss.com/content/images/2024/07/verified-flatpak-apps.png)

如果你启用了未验证的 Flatpak 应用，列表中会出现一个红色盾牌图标，提醒你注意。

**推荐阅读 📖**

{% link https://itsfoss.com/linux-mint-vs-ubuntu/ 8 Reasons Why Linux Mint is Better Than Ubuntu icon:https://itsfoss.com/content/images/2023/07/why-mint-is-better-than-ubuntu.png %}

## 新应用

我们可以看到，在 Linux Mint 22 中预装了一个 Matrix 客户端「Element」，它作为 Firefox 网络应用存在，可让你连接到 Linux Mint 社区以获得支持或进行讨论。你可以在应用列表中找到它，名为「Matrix」。

当然，你也可以使用它来添加其他 Matrix 频道，并与使用去中心化 Matrix 网络的其他人建立联系。

![linux mint element 应用](https://itsfoss.com/content/images/2024/07/linux-mint-22-element.png)

此外，还有一个新的 XApp，即 **GNOME Online Accounts GTK**。在 GNOME 46 将其在线账户功能后端迁移到 GTK 4 后，它不再与使用 GTK 3 的 Cinnamon、Budgie、Unity 兼容，因此开发了这个替代应用。

![gnome 在线账户 GTK](https://itsfoss.com/content/images/2024/07/online-accounts-gtk.png)

现在，借助独立的 GTK 在线账户 XApp，它也进入了 Xfce 和 MATE 桌面环境，这可能是很有用的补充。

## Linux 内核更新

![linux mint neofetch 截图](https://itsfoss.com/content/images/2024/07/linux-mint-22-neofetch.png)

Linux Mint 22 采用了 [Linux 内核 6.8](https://news.itsfoss.com/linux-kernel-6-8-release/)。此版本支持较新的 AMD 显卡和 Intel Xe 显卡硬件。

## 系统资源使用情况

搭载 Cinnamon 桌面环境的 Linux Mint 一如既往地对系统资源要求不高。如果你想要更注重轻量级的体验，可以选择 Xfce 版本。

不过，它在至少配备 4 GB 内存的各种现代系统上都能流畅运行。以下是全新安装 Linux Mint 后的资源使用情况：

![linux mint 22 系统资源使用情况](https://itsfoss.com/content/images/2024/07/linux-mint-22-resources.png)

## 有意义的改进和其他变化

Linux Mint 以保留用户始终喜欢的特性而闻名，即使它所基于的 Ubuntu 版本决定改变某些方面。

例如，和 Mozilla Firefox 一样，Thunderbird 以 Snap 包而非 .deb 包的形式提供。然而，**Linux Mint 仍将默认提供 Thunderbird 的 .deb 包**，并会继续维护。

还有一些细微的改进，包括：

- 在 [Timeshift 备份](https://itsfoss.com/backup-restore-linux-timeshift/) 工具中删除快照时会显示额外的确认对话框。
- 便签应用可以从命令行调用。
- xfce4-xapp-status-plugin 系统托盘小程序支持对全彩色和符号图标进行可配置的图标大小设置。
- 声音服务器切换到 Pipewire。

**推荐阅读 📖**

{% link https://itsfoss.com/backup-restore-linux-timeshift/ Guide to Backup and Restore Linux Systems with Timeshift icon:https://itsfoss.com/content/images/2023/07/data-backup-with-timeshift.png %}

## Linux Mint 22 扬其所长

Linux Mint 是一个可靠的 Ubuntu 替代方案，其安全更新支持至 2029 年。

如果你不喜欢 Ubuntu 的某些选择，或者你喜欢在任何桌面环境中运行的 Linux Mint XApps 所提供的一致体验，那么你会想尝试 Linux Mint 而不是其他基于 Ubuntu 的发行版。

显而易见，**Linux Mint 名副其实，在 Linux 发行版的世界中是一股清流**。**它在为桌面体验添加现代元素的同时，仍不忘提供实用的功能**。

你可以按照我们的 Linux Mint 22 升级教程开始操作，或者直接进行全新安装（如果你已经备份好了数据）：

{% note color:yellow 📋 在我发布这篇文章时，升级可能尚未可用。升级功能需要几天时间才能正常使用。升级步骤应该与上次升级相同。  %}

{% link https://itsfoss.com/upgrade-linux-mint-version/ How to Upgrade to Linux Mint 21 [Step by Step Tutorial] icon:https://itsfoss.com/content/images/wordpress/2018/07/upgrade-to-linux-mint-21.png %}

*💬 你试过 Linux Mint 22 了吗？你对这次升级有什么看法？请在下面的评论中告诉我。*