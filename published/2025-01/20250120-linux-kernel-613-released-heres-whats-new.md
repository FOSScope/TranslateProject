---
title: "Linux 内核版本 6.13 发布：以下是新增的内容！"
date: 2025-01-26 06:40:24
abbrlink: 20250120-linux-kernel-613-released-heres-whats-new
author:
  - fosscope-translation-team
  - claude-35-sonnet
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2025/01/linux-kernel-613-released-heres-whats-new/linux-kernel-6-13-release.webp
cover: https://static.fosscope.com/articles_img/2025/01/linux-kernel-613-released-heres-whats-new/linux-kernel-6-13-release.webp
categories:
  - 翻译
  - 新闻
tags:
  - Linux
  - Linux Kernel
  - Linux 内核
authorInfo: |
  via: https://news.itsfoss.com/linux-kernel-6-13/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：Claude 3.5 Sonnet
  校对：[Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: true # 是否已校对完成
published: true # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

AMD 和老款 Apple 设备的用户，这次发布对你们来说是个好消息！

<!-- more -->

按照惯例，新的 Linux 内核版本如期而至，带来了众多改进。在上一版本发布仅两个月后，它延续了我们所熟悉的快速开发周期。

Linus Torvalds 分享了他对这次发布的 [一些想法](https://lore.kernel.org/lkml/CAHk-=wiprabAQcCwb3qNhrT5P50MJNqunC9JU5v99kdvM-2rsg@mail.gmail.com/T/)：

> 上周没有发生任何可怕或意外的事情，所以我已经标记并推送了最终的 6.13 版本。
> 
> 其主要是一些最终的驱动程序修复（主要是 GPU 和网络方面 —— 这很正常），还有一些文档更新。
> 此外还有各种小改动。简短日志附在下面，供想要查看细节的人参考（一如既往，这只是上周的简短日志，完整的 6.13 日志显然太大了）

## Linux 内核 6.13：有什么新特性？

与 [上一版本](https://news.itsfoss.com/linux-kernel-6-12/) 不同，Linux 6.13 **不是长期支持（LTS）版本**，因此，在其生命周期结束前，预计将有一段较短的官方维护和更新期 —— 通常在 9-12 周左右。

如果你需要更长时间的支持，继续使用 LTS 版本会是更好的选择。

让我们现在来看看这个版本的**主要亮点**：

* **AMD 升级**
* **Intel 改进**
* **其他变更**

### AMD 升级

{% image https://static.fosscope.com/articles_img/2025/01/linux-kernel-613-released-heres-whats-new/amd-imporvements.png %}

[AMD 3D V-Cache](https://www.amd.com/en/products/processors/technologies/3d-v-cache.html) 处理器的用户会很高兴听到 Linux 内核 6.13 带来了**性能优化驱动**，有助于改善此类处理器在 Linux 上的性能。

如果你不了解，3D V-Cache 是一种在处理器顶部堆叠额外 L3 缓存的技术，用于提升会受益于大容量、快速缓存内存的各种工作负载下的性能。AMD 与台积电合作，使用他们的 [3DFabric](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/3DFabric.htm) 技术实现了这一突破。

在图形方面，*AMDGPU/AMDKFD* 内核驱动程序得到改进，使 *AMDGPU 显示核心 (DC)* 代码能够在 [龙架构](https://zh.wikipedia.org/wiki/%E9%BE%99%E8%8A%AF) 硬件上正确构建。这使得最新的 AMD Radeon GPU 可以在搭载龙架构的系统上工作。

同样，还有一项升级为 [Radeon RX 7000 系列](https://en.wikipedia.org/wiki/Radeon_RX_7000_series) 显卡启用了"*零转速*"风扇功能。这种模式允许在 GPU 温度较低时风扇保持静止，在轻负载或空闲期间减少噪音和功耗。

### Intel 改进

{% image https://static.fosscope.com/articles_img/2025/01/linux-kernel-613-released-heres-whats-new/intel.webp %}

另一方面，也有许多针对 Intel 的改进，首先是 **Xe3 显卡的初始显示支持**，其将在即将推出的 Panther Lake 处理器上首次亮相。这些处理器计划在2025年年中推出，但情况可能会有变化。

这一版本还为即将发布的面向数据中心的 Intel Xeon [Clearwater Forest](https://www.intel.com/content/www/us/en/foundry/library/advanced-process-technologies-for-data-center.html) 处理器做了额外准备。Linux 内核现在通过 IFS 驱动程序包含了 [现场扫描](https://www.intel.com/content/www/us/en/support/articles/000099537/processors/intel-xeon-processors.html)（*In-Field Scan, IFS*）支持，允许在部署期间进行硅测试，并在硬件老化时进行后续监控。

### 其他变更

我们以一些其他有趣的变更来结束这部分内容：

* 包含 EXT4 和 XFS 的原子写入支持。
* 改进了 USB4 调试时的行为。
* 支持许多较旧的 Apple iPad 和 iPhone 设备。
* 龙芯 CPU 的实时内核支持（*PREEMPT\_RT*）。
* 支持 Secure Digital Ultra Capacity (*SDUC*) 规范的存储卡。

## 安装 Linux 内核 6.13

如果你正在运行 [滚动发布](https://itsfoss.com/rolling-release/) 版本的发行版，那么你将是最先收到这个内核版本的用户之一。但对于我们其他人来说，我们需要等待我们的发行版在点发布或主要发布中提供它。

然而，如果你等不及的话，那么你可以尝试在 Ubuntu 中 [安装最新的主线 Linux 内核](https://itsfoss.com/upgrade-linux-kernel-ubuntu/)。记住，这是一个有风险的更改，建议先备份你的数据。

你可以在 [官方网站](https://www.kernel.org/) 上找到 Linux 6.13 的压缩包。

<center>{% button "Linux kernel 6.13" https://www.kernel.org/ %}</center>
