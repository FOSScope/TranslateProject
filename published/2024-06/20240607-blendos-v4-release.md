---
title: 带有安卓应用支持的 blendOS v4 现已发布
date: 2024-06-09 10:00:00
abbrlink: 134154de
author:
  - fosscope-translation-team
  - Cubik65536
  - cys2004
banner: https://static.fosscope.com/articles_img/2024/06/blendos-v4-release/cover.png
cover: https://static.fosscope.com/articles_img/2024/06/blendos-v4-release/cover.png
categories:
  - 翻译
  - 新闻
tags:
  - Linux
  - blendOS
  - Android
  - Linux 发行版
authorInfo: |
  via: https://news.itsfoss.com/blendos-v4-release/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[Cubik65536](https://github.com/Cubik65536)
  校对：[cys2004](https://github.com/cys2004)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

blendOS 的下一个重大升级已经到来

<!-- more -->

blendOS 是一个基于 Arch Linux 的，[面向未来的不可变 Linux 发行版](https://itsfoss.com/immutable-linux-distros/?ref=news.itsfoss.com)，也是前者的独特不可变和<ruby>原子变体<rt>atomic variant</rt></ruby>。

我之前曾在报道 [blendOS v3 的发布](https://news.itsfoss.com/blendos-v3-released/) 时了解到了这个项目，那是一个改变游戏规则的版本，带来了全面的重大变化和增加。近一年后，我们现在有了一个新版本。

被开发者们称为「重新定义 blendOS 的开创性版本」，blendOS v4 的发布标志着这个相对较新的 Linux 发行版发展的一个重要的新篇章。

与我一起探索这个新版本吧。

{% note color:green 💡 冷知识：blendOS 的标志灵感来源于我们（译注：It's FOSS）首次报道该项目时的特色图。 %}

## 🆕 blendOS v4：有什么新特性？

![一个 blendOS v4 桌面视图的截图，显示了欢迎和系统详情窗口](https://static.fosscope.com/articles_img/2024/06/blendos-v4-release/blendOS_v4-1.jpg)

作为一个[滚动发行版](https://itsfoss.com/rolling-release/?ref=news.itsfoss.com)，blendOS 总是保持着与 Linux 世界最新进展的同步。

所以，这个版本有 **Linux 内核版本 6.9.3-arch1-1** 为一切提供动力，[GNOME 46](https://news.itsfoss.com/gnome-46-release/) 作为默认桌面环境，同时还提供了其他选项，如 KDE Plasma、Xfce、Budgie 和 MATE。

另外，从这个版本开始，blendOS 已经完全声明式化，允许用户从各种 Arch 仓库和 AUR 安装任何内核、软件包和驱动程序。

你同样可以获得对安卓应用的支持，这可以通过 GNOME 和 KDE Plasma 的 Wayland 会话中的“系统”应用来启用。

而且，还有一个新的 GUI 应用，配合一个 CLI 对应程序，可以让你创建用于模拟其他发行版（如 Debian、Ubuntu、Fedora 和 CentOS）的自定义容器。

当这个功能被使用时，`.deb`、`.rpm` 和 `.apk` 等包将会被安装到它们对应的容器中，用户可以像启动系统上的其他应用一样启动它们。

![一个展示 blendos v4 中容器系统运行情况的截图](https://static.fosscope.com/articles_img/2024/06/blendos-v4-release/blendOS_v4-2.jpg)

开发者们给出了这个功能可能的使用方法：

> 打个比方，一个名为 deb 的 Debian 容器中的 apt 可以在主机 shell 中通过 apt.deb 访问和使用。

> 任何在容器中打开的应用（GUI 或 CLI）都与主机上安装的本地应用无异，并且如果你使用桌面环境，它们会自动出现在应用网格/启动器中。

这让人想起了 [QubesOS](https://news.itsfoss.com/qubes-os-4-2-release/)，它的功能与之相似，但在更基础的层面上实现了这一点。

在任何情况下，要获取更多有关新的 blendOS 发布的详细信息，你可以查看[官方公告博客](https://blendos.co/blog/2024/06/05/blendos-v4-released-arch-linux-made-immutable-declarative-and-atomic/?ref=news.itsfoss.com)。

## 📥 获取 blendOS v4

[blendOS 官网](https://blendos.co/download/?ref=news.itsfoss.com) 列出了许多下载镜像，供你获取 blendOS v4 发布版，但在撰写本文时，其中的许多镜像都处于离线状态。我从德国镜像「Sahilister」下载了这个版本来测试。

<center>{% button "blendOS v4" https://blendos.co/download %}</center>

如果你需要安装帮助，[文档](https://blendos.co/install/?ref=news.itsfoss.com) 是一个很好的起点。你还会发现关于如何使用「tracks」功能切换桌面环境的 [说明](https://blendos.co/install/post-install/arch-user-guide/?ref=news.itsfoss.com#switching-to-other-desktop-environments-or-a-clean-arch-like-system-tracks)，如果默认的桌面环境（GNOME）不适合你的话。

对于那些对开发感兴趣，或者只是想查看源代码的人，可以访问其 [GitLab](https://git.blendos.co/blendOS?ref=news.itsfoss.com) 仓库。
