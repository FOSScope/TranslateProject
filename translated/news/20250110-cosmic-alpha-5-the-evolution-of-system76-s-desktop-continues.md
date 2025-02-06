---
title: COSMIC Alpha 5：System76 桌面环境的进化仍在继续！
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
  - 新闻
tags: 
  - {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/cosmic-alpha-5/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

System76 的 COSMIC 桌面环境正稳步推进！

<!-- more -->

COSMIC 桌面环境距离稳定版发布仍需时日，不过，现在感觉就像在等待《半条命 3》一样。我明白，好东西总是需要时间打磨的，我也很乐意耐心等待。

尽管如此，时不时地，我内心那个狂热的极客还是会忍不住有点小急躁！

不久前，COSMIC 的首个 Alpha 版本发布，让我们得以一窥其开发进展，随后又陆续发布了几个 Alpha 版本。这次，我们将一同探索 COSMIC Alpha 5 版本。让我们来看看有哪些新变化吧。😃

## COSMIC Alpha 5：有何新亮点？

{% image https://news.itsfoss.com/content/images/2025/01/COSMIC_Alpha_5_Fastfetch_Output.jpg '' %}

为了让 COSMIC 更接近稳定版本，Alpha 5 版本带来了一些全新的变化，这些变化也将融入最终版本。首先是 COSMIC 媒体播放器，它现在已成为 **COSMIC 上播放媒体的默认应用程序**。

它使用 Vulkan 进行渲染、使用 VA-API 进行解码（_具体取决于可用性_）以优化视频播放。开发人员还打算在未来增加音频文件播放功能，并提供一个树形视图来管理音频/视频文件。

可变刷新率（_VRR_）的实现也得到了升级。现在，它会考虑显示器的最低刷新率，以确保在运行低于最低刷新率的应用程序中移动光标时不会出现抖动。

{% image https://news.itsfoss.com/content/images/2025/01/COSMIC_Media_Player.png '' %} {% image https://news.itsfoss.com/content/images/2025/01/COSMIC_Alpha_5_Users_Page.png 'COSMIC 媒体播放器和用户设置页面。（来源：System76）' %}

「系统与账户」设置菜单现在新增了 **一个用户页面**，可用于管理系统上的所有用户账户。这允许更改用户名、密码和管理员权限。

在用户界面方面，现在使用 _Alt + Tab_ 和 _Super + Tab_ 组合键时将会按使用活动顺序在应用程序之间切换，依次切换到最近使用的应用程序。同样，COSMIC 终端现在可以打开链接；只需左键单击 URL，即可使用默认的网络浏览器打开它。

此外，还有其他一些值得注意的变化。一些亮点包括：
  * 修复了与 Linux 内核 6.12 的兼容性问题。
  * 现在可以新建文件夹来保存新文件。
  * 现在右键单击或中键单击可关闭上下文菜单。
  * 解决了垂直显示器上截图捕获的问题。

如需了解更多详细信息，你可以查看 System76 的官方博客公告。

## 想亲自测试一下吗？

官方网站提供了适用于英特尔/AMD 和英伟达系统的两个 ISO 镜像，它们均运行 Pop!_OS 24.04 LTS Alpha 版本。

{% note 🚧 '由于这是 **一个仍在开发中的桌面环境** ，我建议你仅将其用于测试，而不要用于生产环境或日常使用。' color:red %}

我在虚拟机上进行了测试，在大部分情况下运行良好，但我无法在 COSMIC 媒体播放器上播放视频。

{% button 'COSMIC Alpha 5' 'https://system76.com/cosmic/' %}