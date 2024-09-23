---
title: Manjaro Linux 推出新不可变版本
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesNIED
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/manjaro-linux-starts-experimenting-with-an-immutable-offering/manjaro-immutable.png
cover: https://static.fosscope.com/articles_img/2024/08/manjaro-linux-starts-experimenting-with-an-immutable-offering/manjaro-immutable.png
categories:
  - 翻译
  - 新闻
tags: 
  - Manjaro
authorInfo: |
  via: https://news.itsfoss.com/manjaro-immutable-experiment

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true
translated: true
proofread: false
published: false
---

如果将不可变作为其核心特性，Manjaro Linux 可能会成为一个更可靠的选择。您对此有何看法？

<!-- more -->

[不可变 Linux 发行版](https://itsfoss.com/immutable-distro/) 是一种核心文件保持不变，根文件系统处于只读状态的操作系统。这种运作方式这种架构显著增强了系统的安全性和稳定性。

这种方式也使得处理更新更加灵活。即使更新失败，操作系统也不会因此变得不可恢复（*Ubuntu 就是这样*）。一些热门的选择包括 [NixOS](https://nixos.org/)、[Vanilla OS](https://news.itsfoss.com/vanilla-os-2-orchid/)、[Fedora Silverblue](https://fedoraproject.org/silverblue/) 等。

你可以在我们的列表中找到更多 [不可变发行版选项](https://itsfoss.com/immutable-linux-distros/)。

当然，并不是每个人都喜欢这样的发行版，有些人认为这只是一种噱头。

这时 [Manjaro Linux](https://manjaro.org/) 就登场了，它是一款深受社区喜爱的 [基于 Arch 的用户友好型发行版](https://itsfoss.com/arch-based-linux-distros/)，可满足各种不同的使用情况。它的开发者们最近发布了一个公告，表示他们已经开始涉足不可变系统的领域。

让我们看看他们都做了些什么。😃

{% note color:red 🚧 这是一个正在开发中的 Linux 发行版，不建议一般使用或生产使用。 %}

## Manjaro 不可变版本：有什么值得期待的？

![a screenshot of an early testing version of manjaro immutable](https://static.fosscope.com/articles_img/2024/08/manjaro-linux-starts-experimenting-with-an-immutable-offering/Manjaro_Immutable_Testing.jpg)

作为**社区测试版本**，Manjaro 不可变版由 [Arkdep](https://github.com/arkanelinux/arkdep) 构建，这是一个用于创建基于 btrfs 的不可变系统的热门工具包；以及 [Arkane Linux](https://news.itsfoss.com/arkane-linux/)，一个“*有主见、不可变、原子化、多根目录的基于 Arch 的发行版*”。

由于这是一个**实验性版本**，Manjaro 的开发者们希望从社区收集反馈，以了解 Manjaro 不可变版背后的技术在日常使用中的表现如何。请记住，这并不保证将来会有一个完整版本。

当被社区成员 [问及](https://forum.manjaro.org/t/manjaro-immutable-out-now-for-community-testing/166364/2) **这是否会成为 Manjaro 的官方变体**时，Manjaro Linux 的首席技术官 [Roman Gilg](https://www.linkedin.com/in/roman-gilg/) 表示：


> 我们确实计划让它成为 Manjaro 的一个官方变体。通过社区测试版本，我们正在收集人们对这个版本的期望和反馈，以及哪些功能还需要加入或可以精简。
>

另外，还有人 [提问](https://forum.manjaro.org/t/manjaro-immutable-out-now-for-community-testing/166364/14) **是否计划推出 ARM 版本**。

对此，Manjaro开发者 [Dennis ten Hoove](https://github.com/dennis1248) 补充说这有可能实现。然而，ARM 版本尚未经过测试，目前没有具体的计划，但未来可能会尝试。

## 📥 获取 Manjaro 不可变版本

你可以从官方下载镜像获取社区测试版 ISO。

你可以选择直接安装在实体机上，或者在 VirtualBox 或 QEMU 虚拟机中运行。请记住，启用 EFI 是强制性的，并且至少需要 32 GB 的存储空间来安装。

<center>{% button "Manjaro 不可变版本（直接下载）" https://download.manjaro.org/manjaro-gnome-immutable/20240801/manjaro-gnome-immutable-2024.08.01-x86_64.iso %}</center>

希望进一步向开发者提供反馈的用户可以通过加入专门的 Matrix 频道，或在 Manjaro 论坛上回复初始公告。

*💬 你期待使用不可变的 Manjaro 吗？在下方告诉我吧！*
