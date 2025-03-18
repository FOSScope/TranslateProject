---
title: Linux 将驱动 Nvidia Project DIGITS，打造你桌面上的 AI 超级计算机
date: 2025-02-04 22:06:19
abbrlink: linux-will-power-nvidia-project-digits-the-ai-supercomputer-on-your-desk
author:
  - fosscope-translation-team
  - excniesnied
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2025/01/linux-will-power-nvidia-project-digits-the-ai-supercomputer-on-your-desk/nvidia-digits-linux-pc.webp
cover: https://static.fosscope.com/articles_img/2025/01/linux-will-power-nvidia-project-digits-the-ai-supercomputer-on-your-desk/nvidia-digits-linux-pc.webp
categories:
  - 翻译
  - 新闻
tags:
  - Linux
  - AI
  - 人工智能
  - Nvidia
  - 英伟达
  - 家庭实验室
authorInfo: |
  via: https://news.itsfoss.com/nvidia-project-digits/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[Churnie HXCN](https://github.com/excniesnied)
  校对：[Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: true # 是否已校对完成
published: true # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

有人感到惊讶吗？反正我不惊讶。Linux 是超级计算机操作系统最佳选择。

<!-- more -->

[人工智能](https://zh.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E6%99%BA%E8%83%BD) 已成为21世纪最受瞩目的领域之一，它成功地颠覆了医疗、娱乐、金融等多个行业，甚至改变了我们与科技互动的方式。

谈及此，唯有一家公司的名字浮现脑海 —— [NVIDIA](https://www.nvidia.com/zh-cn/)。他们比其他巨头更早押注人工智能，而此后的回报堪称惊人，推动其市值一路飙升。

在最近的 [国际消费电子展（CES）](https://www.ces.tech/) 上，NVIDIA 展示了一款新型AI超级计算机，**其体积小巧，可置于桌面**，依托强大的硬件配置和 Linux 驱动的操作系统，实现了高效运行。

让我们一探究竟。😃

## NVIDIA Project DIGITS:

{% image https://static.fosscope.com/articles_img/2025/01/linux-will-power-nvidia-project-digits-the-ai-supercomputer-on-your-desk/NVIDIA_Project_Digits_a.jpg 图片来源：NVIDIA %}

Project DIGITS [搭载与联发科](https://corp.mediatek.com/news-events/press-releases/mediatek-collaborates-with-nvidia-on-the-new-nvidia-gb10-grace-blackwell-superchip-powering-the-nvidia-project-digits-personal-ai-supercomputer) 合作研发的全新 [SoC](https://en.wikipedia.org/wiki/System_on_a_chip)，可提供 **1 PFLOPS 的 FP4 AI 计算性能**。开发者可用其在本机开发和运行 AI 模型推理。

Project DIGITS 搭载 [DGX OS](https://docs.nvidia.com/dgx/dgx-os-6-user-guide/introduction.html) —— **一款基于 Ubuntu 22.04 的 Linux 操作系统**。NVIDIA 对其进行了深度定制，包含多项优化、附加驱动及诊断/监控工具。

开发者还将获得完整的 AI 开发工具链，涵盖 SDK、编排工具、PyTorch 等 AI 框架，以及来自 NVIDIA [NGC 目录](https://catalog.ngc.nvidia.com/) 的预训练模型和资源库。

[NVIDIA NeMo 框架](https://www.nvidia.com/en-us/ai-data-science/products/nemo/) 和 [RAPIDS 库](https://developer.nvidia.com/rapids) 等工具也可使用，助力开发者将工作部署至云端和数据中心。

{% image https://static.fosscope.com/articles_img/2025/01/linux-will-power-nvidia-project-digits-the-ai-supercomputer-on-your-desk/NVIDIA_Project_Digits_b.jpg 图片来源：NVIDIA %}

软件部分介绍完毕，让我们深入了解一下它的硬件规格。Project DIGITS 的**核心配置**包括：

- **SoC:** NVIDIA GB10 Grace Blackwell 超级芯片
- **CPU:** NVIDIA Grace CPU，含 20 个基于 Arm 架构的高能效核心
- **GPU:** NVIDIA Blackwell GPU，配备最新 CUDA 核心与第五代 Tensor 核心
- **内存:** 128 GB 低功耗 DDR5X（CPU 与 GPU 共享）
- **存储:** 最高 4 TB NVMe 固态硬盘
- **连接性:** Wi-Fi、蓝牙和 USB；具体细节待公布
- **性能:** 可运行 200B 参数的大语言模型（LLM）。通过 [NVIDIA ConnectX](https://www.nvidia.com/en-us/networking/ethernet-adapters/) 连接另一台 Project DIGITS 后，可扩展至 405B 参数模型。

欲知详情，请参阅 [官方新闻稿](https://nvidianews.nvidia.com/news/nvidia-puts-grace-blackwell-on-every-desk-and-at-every-ai-developers-fingertips)。

## 何时能入手 NVIDIA Project DIGITS？

若您已心动，还需稍作等待。Project DIGITS 计划于 **2025 年 5 月发货**，售价 **3000 美元**，首发地区尚未明确。

您可通过 NVIDIA [官方网站](https://www.nvidia.com/en-us/project-digits/) 注册，以便在产品上市时通过授权合作伙伴获取更新。

<center>{% button NVIDIA Project DIGITS https://www.nvidia.com/en-us/project-digits/ %}</center>

*💬 您会为您的 [家庭实验室](https://itsfoss.com/tag/homelab/) 添置一台吗？欢迎留言讨论！*
