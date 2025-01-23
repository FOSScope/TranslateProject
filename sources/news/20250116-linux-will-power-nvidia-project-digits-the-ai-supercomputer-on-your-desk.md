---
title: "Linux Will Power Nvidia Project DIGITS, the AI Supercomputer on Your Desk"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/nvidia-project-digits/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: false # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

Who is surprised? Not me. Linux is the best choice for super computer operating systems.

<!-- more -->

[Artificial intelligence](https://en.wikipedia.org/wiki/Artificial_intelligence) has rapidly become one of the most talked-about things of the 21st century, managing to disrupt many industries ranging from healthcare, entertainment, finance, and even changing the way we interact with technology.

When I think about this, only one organization comes to mind: [NVIDIA](https://www.nvidia.com/en-us/). Their investments in AI were earlier than those of other big names, but the returns they have generated since have been nothing short of remarkable, propelling them to eye-watering evaluations.

At the recent [CES](https://www.ces.tech/) event, they unveiled **a new AI supercomputer that fits on a desk** and runs on powerful hardware with a Linux-powered operating system making it all happen.

Let's take a closer look. 😃

## NVIDIA Project DIGITS:

<img alt="a photo that shows the nvidia project digits supercomputer placed on a table besides a monitor, keyboard, and mouse, the background has some indoor plants and a bookshelf near a tall window" height="1080" width="1920" />\<img src="https://news.itsfoss.com/content/images/2025/01/NVIDIA\_Project\_Digits\_a.jpg" class="kg-image" alt="a photo that shows the nvidia project digits supercomputer placed on a table besides a monitor, keyboard, and mouse, the background has some indoor plants and a bookshelf near a tall window" loading="lazy" width="1920" height="1080" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/NVIDIA\_Project\_Digits\_a.jpg 600w, https://news.itsfoss.com/content/images/size/w1000/2025/01/NVIDIA\_Project\_Digits\_a.jpg 1000w, https://news.itsfoss.com/content/images/size/w1600/2025/01/NVIDIA\_Project\_Digits\_a.jpg 1600w, https://news.itsfoss.com/content/images/2025/01/NVIDIA\_Project\_Digits\_a.jpg 1920w" sizes="(min-width: 720px) 720px"\>Source: NVIDIA

Offering up **1 petaflop of FP4 AI compute performance**, Project DIGITS is powered by a new [SoC](https://en.wikipedia.org/wiki/System_on_a_chip) that was made in collaboration with [MediaTek](https://corp.mediatek.com/news-events/press-releases/mediatek-collaborates-with-nvidia-on-the-new-nvidia-gb10-grace-blackwell-superchip-powering-the-nvidia-project-digits-personal-ai-supercomputer). Developers can use this to develop and run inference on AI models locally.

All of this is meant to be done on [DGX OS](https://docs.nvidia.com/dgx/dgx-os-6-user-guide/introduction.html), **an Ubuntu 22.04-based Linux operating system** that has been tailored by NVIDIA to include various optimizations, additional drivers, and diagnostic/monitoring tools.

Additionally, developers will have access to a comprehensive suite of tools and resources for AI development, including SDKs, orchestration tools, AI frameworks like PyTorch, and a wide range of pre-trained models and other resources from the NVIDIA [NGC Catalog](https://catalog.ngc.nvidia.com/).

Tools like the NVIDIA [NeMo](https://www.nvidia.com/en-us/ai-data-science/products/nemo/) framework and [RAPIDS](https://developer.nvidia.com/rapids) libraries are also available. These utilities, alongside others, help developers deploy their work to cloud and data center infrastructure.

<img alt="an illustration that shows an exploded view of nvidia project digits with key features being pointed out" height="601" width="1070" />\<img src="https://news.itsfoss.com/content/images/2025/01/NVIDIA\_Project\_Digits\_b.jpeg" class="kg-image" alt="an illustration that shows an exploded view of nvidia project digits with key features being pointed out" loading="lazy" width="1070" height="601" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/NVIDIA\_Project\_Digits\_b.jpeg 600w, https://news.itsfoss.com/content/images/size/w1000/2025/01/NVIDIA\_Project\_Digits\_b.jpeg 1000w, https://news.itsfoss.com/content/images/2025/01/NVIDIA\_Project\_Digits\_b.jpeg 1070w" sizes="(min-width: 720px) 720px"\>Source: NVIDIA

That was all about the software side of things, now let's dive into the juicy hardware aspect of it. The **key specs** of Project DIGITS include:

* **SoC:** NVIDIA GB10 Grace Blackwell Superchip.
* **CPU:** NVIDIA Grace CPU with 20 power-efficient Arm-based cores.
* **GPU:** NVIDIA Blackwell with latest-gen CUDA cores and fifth-gen Tensor cores.
* **RAM:** 128 GB of low-power DDR5X, which is used by both the CPU and GPU.
* **Storage:** Up to 4 TB NVMe.
* **Connectivity:** Wi-Fi, Bluetooth, and USB; not sure on the specifics yet.
* **Performance:** Capable of running 200-billion-parameter LLMs. When linked with another Project DIGITS via [NVIDIA ConnectX](https://www.nvidia.com/en-us/networking/ethernet-adapters/), this can scale up to 405-billion-parameter models.

The [press release](https://nvidianews.nvidia.com/news/nvidia-puts-grace-blackwell-on-every-desk-and-at-every-ai-developers-fingertips) has more details for those interested in learning more.

## When can we get NVIDIA Project DIGITS?

If you are enthusiastic about getting this, then you will have to wait a bit as Project DIGITS is scheduled **to be shipped sometime in May 2025** with a price tag of **$3,000**. Not sure how many countries will see the availability at launch time.

You can sign up on NVIDIA's [official website](https://www.nvidia.com/en-us/project-digits/) to receive updates when the product becomes available through their authorized partners.

[NVIDIA Project DIGITS](https://www.nvidia.com/en-us/project-digits/)

*💬 Are you going to grab one for your* [*homelab*](https://itsfoss.com/tag/homelab/)*? Let me know below!*
