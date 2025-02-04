---
title: Bootkitty： 首个针对 Linux UEFI 的引导工具包出现了！
date: 2025-01-18 03:49:44
abbrlink: 20241128-bootkitty-the-first-uefi-bootkit-built-for-linux-appears
author:
  - fosscope-translation-team
  - excniesnied
  - Cubik65536
banner: https://news.itsfoss.com/content/images/size/w600/format/webp/2024/11/bootkitty.png
cover: https://news.itsfoss.com/content/images/size/w600/format/webp/2024/11/bootkitty.png
categories:
  - 翻译
  - 新闻
tags: Linux
authorInfo: |
  via: https://news.itsfoss.com/bootkitty-linux/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[excnies](https://github.com/excniesnied)
  校对：[Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: true # 是否已校对完成
published: true # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

没有绝对的安全。不过，无需过度担心，只要您遵循最佳安全实践，就能有效防范这类威胁。

<!-- more -->

如果你拥有一台电脑，就必须投入时间和资源来保护它的安全。 全世界的 [恶意攻击者](https://en.wikipedia.org/wiki/Threat_actor) 一直在想方设法破坏电脑的安全。 不管你是个人还是收入丰厚的大公司，都应保持警惕。

曾经，Windows 和 macOS 等操作系统是这类犯罪分子的**主要目标**，但现在并非如此。

随着个人和企业对 Linux 发行版的使用不断增加，它们逐渐成为下一个重要的攻击目标。最近，[一种名为「Bootkitty」的新恶意程序被发现](https://www.welivesecurity.com/en/eset-research/bootkitty-analyzing-first-uefi-bootkit-linux/)，专门针对配备 UEFI 的 Linux 系统。

## Linux 用户需要担心 Bootkitty 吗

{% image https://news.itsfoss.com/content/images/2024/11/Bootkitty_a-1.png 来源：<a href="https://news.itsfoss.com/bootkitty-linux/#:~:text=Source%3A-,ESET,-Known%20for%20their">ESET</a> %}

知名网络安全公司 ESET 的研究人员首次在 [VirusTotal](https://www.virustotal.com/gui/file/f1f84819bdf395d42c36adb36ded0e7de338e2036e174716b5de71abc56f5d40) 上发现了这一恶意程序，该程序被匿名上传为一个未知的 UEFI 应用「*bootkit.efi*」。

ESET 团队对其进行分析后发现，这是**一款针对特定版本 Ubuntu 的 Linux UEFI 引导工具包**。

如果你不知道，[引导工具包](https://en.wikipedia.org/wiki/Rootkit) 是一种专门设计用来感染电脑引导过程的<ruby>隐匿软件<rt>Rootkit</rt></ruby>。这些工具包可以让攻击者在避开常规恶意软件移除方法的同时执行一系列恶意操作。

研究人员推断，Bootkitty 的主要目的是：

> 禁用内核的签名验证功能，并通过 Linux 的 init 进程预加载两个未知的 ELF 二进制文件。

就目前而言，Bootkitty 可以在攻击者已经成功安装了恶意证书的情况下**影响启用了安全启动的 UEFI 系统**。未启用安全启动的系统也可能受其影响。

研究人员发现了许多帮助他们了解这个引导工具包的性质的 [恶意软件痕迹](https://www.sciencedirect.com/topics/computer-science/malware-artifact)。他们发现了两个未使用的函数，这些函数在执行过程中能够打印特殊的 [字符串](https://en.wikipedia.org/wiki/String_(computer_science))。

第一个是上面看到的 ASCII 字符画，这使 ESET 认为 Bootkitty 就是这个引导工具包的名称。


{% grid %}
<!-- cell -->
{% image https://news.itsfoss.com/content/images/2024/11/Bootkitty_b.png %}
<!-- cell -->
{% image https://news.itsfoss.com/content/images/2024/11/Bootkitty_c.png 来源：<a href="https://www.welivesecurity.com/en/eset-research/bootkitty-analyzing-first-uefi-bootkit-linux/">ESET</a> %}
{% endgrid %}

第二个是包含可能的 Bootkitty 作者（*已被 ESET 抹除*）和其他与恶意软件相关的人的列表，以及在每次启动时被打印出来的另一组字符串，其中包含以下文本：

> Bootkitty's Bootkit
> \- Developed By BlackCat
> 
> （翻译：）
> Bootkitty 的引导工具包
> \- 由 BlackCat 开发

ESET 澄清，他们不认为这与臭名昭著的 [BlackCat](https://en.wikipedia.org/wiki/BlackCat_(cyber_gang)) 勒索软件团伙有关，因为该团伙主要开发基于 Rust 的恶意软件，而 Bootkitty 是用 C 语言开发的。

目前，网络安全领域的许多人士认为 Bootkitty 是**一个初步的概念验证引导工具包**，根据 ESET 的数据，它尚未在现实世界中使用。

所以，目前没有必要惊慌。🤓

然而，**采取一些预防措施将大大有助于保护你的 Linux 系统**。你可以下面内容了解一些方法。

## 应该采取哪些措施？

首先，**保持安全启动启用**，因为你的系统很可能尚未受到 Bootkitty 攻击者的恶意 UEFI 证书的影响。其次是最重要的一点：**保持你的 Linux 发行版更新到最新版本**；如果你运行的是过时/不受支持的版本，请进行升级。

此外，ESET 提到要始终**保持你的 [UEFI 撤销列表](https://uefi.org/revocationlistfile) 更新**，以防止恶意引导程序加载并破坏你的系统。你还可以遵循我们文章中提到的一些提示，以 [提高 Linux 系统的安全性](https://itsfoss.com/improve-security-linux/)。

如果你对 Bootkitty 的内部工作原理感兴趣，我强烈建议你阅读 [ESET 的深度博客](https://www.welivesecurity.com/en/eset-research/bootkitty-analyzing-first-uefi-bootkit-linux/)。

对于样本和入侵指标（*IoCs*），你可以访问 ESET 的 [GitHub 仓库](https://github.com/eset/malware-ioc/tree/master/bootkitty)。
