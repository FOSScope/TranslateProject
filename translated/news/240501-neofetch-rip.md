---
title: 不好了！Neofetch 已经不复存在了！
date: 2024-05-01 13:14:52
author:
  - fosscope-translation-team
  - excniesnied
  - <校对者ID>
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/05/neofetch-is-no-more.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/05/neofetch-is-no-more.png
categories:
  - 翻译
  - 新闻
tags:
  - Neofetch
  - Linux
  - CLI
  - Kiss Linux
  - Fastfetch
authorInfo: |
  via: https://news.itsfoss.com/neofetch-rip/

  作者：[SOURAV RUDRA](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[excniesnied](https://github.com/excniesNIED)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

它曾是许多人的最爱。如今，它已不复存在。

<!-- more -->

啊？Neofetch，是一款我们很多人在 [r/unixporn](https://www.reddit.com/r/unixporn/) 甚至 [It's FOSS社区](https://itsfoss.community/) 上展示我们酷炫的 Linux 系统时用到的工具。它是一种 CLI 工具，已经成为 Linux 社区的代名词。

不过，关于 Neofetch 有一些坏消息。让我们深入了解一下。

## 美好的事物总会结束？

![Neofetch](https://news.itsfoss.com/content/images/2024/05/Neofetch.png)

**2024 年 4 月 26 日**，Neofetch 的首席开发者 [dylanaraps](https://github.com/dylanaraps) 将 [Neofetch 的 GitHub 仓库](https://github.com/dylanaraps/neofetch) 归档，并使其转变为只读模式。这表明，**从此之后，Neofetch 将不再有新的开发活动**。

虽然人们可以复制这个仓库，并在此基础上构建新东西，但作为一个独立工具的 Neofetch 已经到此为止了。

令人惊讶的是，**他们还将所有其他 GitHub 仓库全部归档了**，其中另一个热门项目 [Kiss Linux](https://kisslinux.org/) 也被砍掉了。

在我看来，这种事迟早会发生，只是我们永远不知道具体会在何时。你瞧，首席开发者 [过去就有过突然人间蒸发](https://www.reddit.com/r/linux/comments/m4pwix/what_happened_to_k1ss_linux_and_dylan_araps/)，并且没有给出任何明确的解释或说明情况。

在归档所有 GitHub 仓库的同时，dylanaraps 还在 [README 文件](https://github.com/dylanaraps/dylanaraps/blob/master/README.md) 中添加了以下内容：

> 回家种地去了

我想这不言自明吧？无论他们结束运营的原因或情况如何，我们只能向前看。

对于 Neofetch 的用户来说无需担忧，因为有很多替代工具可供选择。它们性能表现同样出色，甚至更胜一筹。

其中，**Fastfetch** 就是一种替代方案，它主要用 C 语言编写，是**一个更快替代工具**。它是一个跨平台的系统信息获取 CLI 工具，可在 **Linux、FreeBSD、Android、Windows 和 macOS** 上运行。

![Fastfetch](https://news.itsfoss.com/content/images/2024/05/Fastfetch.png)

你不必担心更新问题，因为它**正在积极开发中**，有一个很棒的社区支持它，并定期为其做出贡献。需要注意的是，当你在互联网上分享 Fastfetch 截图时，**你的本地 IP 地址也会暴露出来**。

你可以保留图片上的 IP 地址。如果你不希望 IP 地址被暴露，你可以使用 [Obfuscate](https://news.itsfoss.com/obfuscate/) 等工具将其「模糊」处理。

许多 Linux 发行版的软件仓库中都有 Fastfetch。不过，多数版本都比较老旧。你可以从 [GitHub 仓库](https://github.com/fastfetch-cli/fastfetch) 中获取最新的 Fastfetch 版本。

<center>{% button Fastfetch https://github.com/fastfetch-cli/fastfetch %}</center>

*💬 你使用过 Fastfetch 吗？是否更喜欢 Neofetch 的其他系统信息获取 CLI 工具？告诉我你的想法！*

感谢 [Joey](https://www.omgubuntu.co.uk/2024/04/neofetch-system-info-tool-is-dead) 让我们了解到这个消息。😃

