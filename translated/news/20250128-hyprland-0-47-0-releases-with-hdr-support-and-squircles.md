---
title: Hyprland 0.47.0 正式发布：支持 HDR 与圆角窗口
date: {{release_date}}
abbrlink: 
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2025/01/Hyprland-0-47-0-release.webp
cover: https://static.fosscope.com/articles_img/2025/01/Hyprland-0-47-0-release.webp
categories:
  - 翻译
  - 新闻
tags: 
  - Linux
  - Hyprland
  - 窗口管理器
authorInfo: |
  via: https://news.itsfoss.com/hyprland-0-47-0-release/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesnied](https://github.com/excniesnied)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
<<<<<<< HEAD
translated: true # 是否已翻译完成
=======
translated: false # 是否已翻译完成
>>>>>>> 8aa253a64997b408c10828b2cfba44b63095e405
proofread: false # 是否已校对完成
published: false # 是否已发布
---

你会注意到这次 Hyprland 更新带来了许多实用变化，从窗口圆角到首次支持 HDR。

<!-- more -->

Hyprland 是当下最受欢迎的新兴动态平铺窗口合成器。它凭借惊艳的视觉效果潜力（远超传统枯燥的桌面环境）以及在 Wayland 会话中的卓越性能表现，迅速收获了大批忠实用户。

尽管距离稳定的 1.0 版本尚有时日，但当前发布的一系列版本已经足以让追求个性化 Linux 美化的用户满意。

近日，Hyprland 首席开发者宣布推出 0.47.0 新版更新。让我们一探究竟。😄

## 🆕 Hyprland 0.47.0：新特性速览

{% image https://static.fosscope.com/articles_img/2025/01/Hyprland_Banner.png '' %}

最引人注目的当属新增的**窗口圆角（_rounded edges_）支持** ，这使得 Hyprland 能够与其他主流方案看齐。其次是**实验性 HDR 与色彩管理支持**的加入，这对于提升视觉质量和精准度意义重大，尤其对高端显示器用户而言。

此外还实现了 _hyprland_surface_ 和 _hyprland_lock_notify_ ，优化了屏幕锁定和系统休眠时的行为。

{% image https://static.fosscope.com/articles_img/2025/01/Hyprland_Donation_Request.png '' %} {% image https://static.fosscope.com/articles_img/2025/01/Hyprland_Squircles.png 'Hyprland 0.47.0 圆角效果与捐赠提醒弹窗截图。（来源：<a href="https://github.com/vaxerski/?ref=news.itsfoss.com">Vaxry</a>）' %}

与 KDE 类似，Hyprland 现在新增了"捐赠提醒"功能——**每年 7 月和 12 月会弹出两次捐赠提示**，鼓励用户支持项目持续发展。

_虽然存在关闭该提示的命令，但在此处恕不透露。_ 😠

其他值得关注的改进包括：

* 修复 XWayland 下的光标显示异常
* 新增 GPU 热插拔支持
* hyprpm 新增强制重载所有插件选项
* 优化了 NVIDIA 硬件之外的 CTM（ _用于 hyprsunset_ ）的过渡效果

你可以通过官方博客公告来了解本次更新的完整细节。

## 📥 获取 Hyprland 0.47.0

由于开发者已停止提供预编译版本，用户需通过源码自行构建。相关文件可在 GitHub 仓库获取。

{% button 'Hyprland 0.47.0' 'https://github.com/hyprwm/Hyprland/releases/tag/v0.47.0' %}

若需在 Linux 系统上安装 Hyprland，建议参考我们的详细指南。我们的教程涵盖了其在所有主流发行版上的安装步骤，助你轻松上手。
