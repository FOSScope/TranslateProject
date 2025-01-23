---
title: "Linux Kernel 6.13 Released: Here's What's New!"
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
  via: https://news.itsfoss.com/linux-kernel-6-13/

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

AMD users and old Apple device owners, this is a good release for you!

<!-- more -->

As usual, a new Linux kernel release has arrived on schedule, bringing numerous improvements. Released just two months after the previous version, it continues the fast-paced development cycle we've come to expect.

Linus Torvalds has shared [some of his thoughts](https://lore.kernel.org/lkml/CAHk-=wiprabAQcCwb3qNhrT5P50MJNqunC9JU5v99kdvM-2rsg@mail.gmail.com/T/) about this release:

> So nothing horrible or unexpected happened last week, so I've tagged  
> and pushed out the final 6.13 release.  
>   
> It's mostly some final driver fixes (gpu and networking dominating -  
> normal), with some doc updates too. And various little stuff all over.  
> The shortlog is appended for people who want to see the details (and,  
> as always, it's just the shortlog for the last week, the full 6.13 log  
> is obviously much too big)

## Linux Kernel 6.13: What's New?

Unlike the [previous release](https://news.itsfoss.com/linux-kernel-6-12/), Linux 6.13 is **not a long-term support (LTS) release**, so expect a short period of official maintenance and updates—typically around 9–12 weeks—before it reaches end-of-life.

If you need longer support, sticking with an LTS release is a better option.

Let's dive into the **key highlights** of this release now:

* **AMD Upgrades**
* **Intel Refinements**
* **Miscellaneous Changes**

### AMD Upgrades

<img alt="amd linux kernel" height="506" width="900" />\<img src="https://news.itsfoss.com/content/images/2025/01/amd-imporvements.png" class="kg-image" alt="amd linux kernel" loading="lazy" width="900" height="506" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/amd-imporvements.png 600w, https://news.itsfoss.com/content/images/2025/01/amd-imporvements.png 900w" sizes="(min-width: 720px) 720px"\>

Owners of [AMD 3D V-Cache](https://www.amd.com/en/products/processors/technologies/3d-v-cache.html) CPUs will be happy to hear that Linux kernel 6.13 ships with **a performance optimizer driver** that helps improve the performance and handling of such processors on Linux.

If you didn't know, 3D V-Cache is a technique where additional layers of L3 cache are stacked on top of a processor to improve performance across various workloads that benefit from large, fast cache memory. AMD pulled this off in collaboration with TSMC, using their [3DFabric](https://3dfabric.tsmc.com/english/dedicatedFoundry/technology/3DFabric.htm) tech.

In the graphics department, the *AMDGPU/AMDKFD* kernel driver was improved to allow the *AMDGPU Display Core (DC)* code to build properly on [LoongArch](https://en.wikipedia.org/wiki/Loongson) hardware. This enables recent AMD Radeon GPUs to work on LoongArch-equipped systems.

Similarly, there is an upgrade that enables the “*zero RPM*” fan feature for the [Radeon RX 7000 series](https://en.wikipedia.org/wiki/Radeon_RX_7000_series) of graphics cards. This mode allows the fans to remain idle when the GPU temperature is low, reducing noise and power consumption during lighter workloads or idle periods.

### Intel Refinements

<img alt="intel improvements" height="506" width="900" />\<img src="https://news.itsfoss.com/content/images/2025/01/intel.png" class="kg-image" alt="intel improvements" loading="lazy" width="900" height="506" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/intel.png 600w, https://news.itsfoss.com/content/images/2025/01/intel.png 900w" sizes="(min-width: 720px) 720px"\>

On the other side, there are many refinements for Intel too, starting with **initial display support for Xe3 graphics**, which is set to debut on the upcoming Panther Lake CPUs. These processors are set for a mid-2025 launch, but things could change.

There is also additional preparation for the upcoming Intel Xeon [Clearwater Forest](https://www.intel.com/content/www/us/en/foundry/library/advanced-process-technologies-for-data-center.html) CPUs, which are aimed at data centers. The Linux kernel now includes support for [In-Field Scan](https://www.intel.com/content/www/us/en/support/articles/000099537/processors/intel-xeon-processors.html) (*IFS*) via the IFS driver, allowing for silicon testing during deployment and later monitoring as the hardware ages.

### Miscellaneous Changes

We wrap this up with some other interesting changes that include:

* Inclusion of atomic write support for EXT4 and XFS.
* Improved behavior when performing USB4 debugging.
* Support for many older Apple iPad and iPhone devices.
* Real-Time kernel support (*PREEMPT\_RT*) for LoongArch CPUs.
* Support for Secure Digital Ultra Capacity (*SDUC*) memory cards.

## Installing Linux Kernel 6.13

If you are running a [rolling release](https://itsfoss.com/rolling-release/) distro, then you will be among the first ones to receive this kernel release on your system. But, for the rest of us, we will have to wait before our distro offers it as part of a point release or a major release.

However, if you can't wait, then you can try [installing the latest mainline Linux kernel in Ubuntu](https://itsfoss.com/upgrade-linux-kernel-ubuntu/). Just remember that this is a risky change, and backing up your data is recommended.

You can find the tarball for Linux 6.13 on the [official website](https://www.kernel.org/).

[Linux kernel 6.13](https://www.kernel.org/)
