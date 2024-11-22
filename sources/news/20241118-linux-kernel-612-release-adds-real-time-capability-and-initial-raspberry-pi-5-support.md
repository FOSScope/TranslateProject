---
title: "Linux Kernel 6.12 Release Adds Real-Time Capability and Initial Raspberry Pi 5 Support"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/11/linux-kernel-6-12-release.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/11/linux-kernel-6-12-release.png
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/linux-kernel-6-12/

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

Linux Kernel 6.12 finally brings in real-time computing capabilities to the mainline.

<!-- more -->

Every two or three months, we get a new kernel release with numerous improvements and Linus's thoughts on it.

Now is the time for a brand-new release, i.e., **Linux kernel 6.12**.

It brings in plenty of interesting changes, and other refinements. And, I am sure, you will find some new feature changes very cool!

As usual, Linus Torvalds had something to [add](https://lore.kernel.org/lkml/CAHk-=wgtGkHshfvaAe_O2ntnFBH3EprNk1juieLmjcF2HBwBgQ@mail.gmail.com/T/):

> No strange surprises this last week, so we're sticking to the regular  
> release schedule, and that obviously means that the merge window opens  
> tomorrow. I already have two dozen+ pull requests in my mailbox, kudos  
> to all the early birds.

## Linux Kernel 6.12: What's New?

For starters, this is expected to be a [Long-Term Support](https://itsfoss.com/long-term-support-lts/) (LTS) release that will remain supported for two years, until 2026. The various distribution maintainers can choose to extend support for the kernel by backporting patches or adding new ones.

Let me dive in to the **key highlights** of this release:

* **Real-time PREEMPT\_RT**
* **Intel Improvements**
* **Better Laptop Support**
* **AMD & RISC-V Upgrades**

### Real-Time PREEMPT\_RT

<img alt="real time linux kernel representation by a clock gear icon" height="890" width="1336" />\<img src="https://news.itsfoss.com/content/images/2024/11/linux-6-12-rt.png" class="kg-image" alt="real time linux kernel representation by a clock gear icon" loading="lazy" width="1336" height="890" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/linux-6-12-rt.png 600w, https://news.itsfoss.com/content/images/size/w1000/2024/11/linux-6-12-rt.png 1000w, https://news.itsfoss.com/content/images/2024/11/linux-6-12-rt.png 1336w" sizes="(min-width: 720px) 720px"\>

The support for PREEMPT\_RT in the mainline kernel has been in the making for more than a decade now, and it finally saw the light with the Linux kernel 6.12 release.

In simpler terms, it is a technical improvement that should give you a better response time for the tasks you run, and boost the performance overall.

Of course, it is tough for an end-user to notice the difference; however, this makes the Linux kernel's real-time computing capabilities complete, and more enterprise-grade for factories, healthcare, telco, and automotive industries.

And, this improvement is ready for ARM64, RISC-V, and X86/X86\_64 as well.

In case you did not know, Canonical managed to bring this a little early with its [Real-time Ubuntu](https://ubuntu.com/real-time) offering. You can go through the official blog posts on it to learn more about real-time Linux:

[

What is real-time Linux? Part I | Ubuntu

Welcome to this three-part blog series on real-time Linux. Throughout the series, we will assess the key features of a real-time system. We will understand how a real-time capable Linux kernel differs from mainline, and touch upon the performance trade-offs you should consider when choosing real-time versus a low-latency kernel, for inst […]

![]()\<img class="kg-bookmark-icon" src="https://assets.ubuntu.com/v1/f38b9c7e-COF%20apple-touch-icon.png" alt=""\>UbuntuEdoardo Barbieri

![]()\<img src="https://ubuntu.com/wp-content/uploads/0406/Real\_Time\_Linux\_Part1.png" alt=""\>

](https://ubuntu.com/blog/what-is-real-time-linux-i)

### Intel Improvements

<img alt="linux kernel intel improvements, an image with intel logo" height="890" width="1336" />\<img src="https://news.itsfoss.com/content/images/2024/11/linux-6-12-intel.png" class="kg-image" alt="linux kernel intel improvements, an image with intel logo" loading="lazy" width="1336" height="890" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/linux-6-12-intel.png 600w, https://news.itsfoss.com/content/images/size/w1000/2024/11/linux-6-12-intel.png 1000w, https://news.itsfoss.com/content/images/2024/11/linux-6-12-intel.png 1336w" sizes="(min-width: 720px) 720px"\>

Introduced as part of this release is support for Intel [uncore](https://en.wikipedia.org/wiki/Uncore) and power events for Arrow Lake and Lunar Lake, with additional improvements for hybrid P/E-core handling for some Lunar Lake processors.

There are also some updates for the [perf](https://perfwiki.github.io/main/) subsystem, such as per-PMU context rescheduling for improved single-[PMU](https://cloud.google.com/compute/docs/pmu-overview) performance, a fix for a long-standing bug, and implementation of [RCU](https://en.wikipedia.org/wiki/Read-copy-update)-protected hot path optimizations for improved performance.

Furthermore, Intel has started **initial enablement work for the upcoming Panther Lake and Diamond Rapids Xeon processors**, adding the model numbers to the kernel, and introducing HDMI support for Panther Lake.

On the graphics side, Linux 6.12 enables [Xe2](https://www.intel.com/content/www/us/en/content-details/824434/2024-intel-tech-tour-xe2-and-lunar-lake-s-gpu.html) and Battlemage GPUs by default, with the Intel graphics driver now reporting the fan speed of GPUs via HWMON.

### Better Laptop Support

<img alt="linux kernel 6.12 laptop" height="890" width="1336" />\<img src="https://news.itsfoss.com/content/images/2024/11/linux-6-12-laptop.png" class="kg-image" alt="linux kernel 6.12 laptop" loading="lazy" width="1336" height="890" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/linux-6-12-laptop.png 600w, https://news.itsfoss.com/content/images/size/w1000/2024/11/linux-6-12-laptop.png 1000w, https://news.itsfoss.com/content/images/2024/11/linux-6-12-laptop.png 1336w" sizes="(min-width: 720px) 720px"\>

Similarly, there are many updates for laptops in this kernel release. There is now the ASUS WMI driver for supporting fan profiles on [Vivobook](https://www.asus.com/laptops/for-home/vivobook/) laptops, the ThinkPad ACPI driver for fan control on the [ThinkPad Edge E531](https://psref.lenovo.com/syspool/Sys/PDF/withdrawnbook/ThinkPad_E531_WE.pdf), and extended battery configuration support for recent Dell laptops.

I am particularly looking forward to the Dell upgrade, as I don't have to go into the BIOS to change between the various battery modes on my laptop anymore.

There's also better support for LG and Panasonic laptops. You can learn more about these laptop upgrades in the [GIT pull](https://lore.kernel.org/lkml/dede57b5-3ef2-4451-a496-537f3c05a1d6@redhat.com/).

### AMD & RISC-V Upgrades

AMD's engineers have been busy working on RDNA 4 hardware support, alongside new things like OverDrive overclocking for SMU 14.x hardware, better support for AMD Instinct accelerators, and various graphics command processor padding optimizations.

For RISC-V, there is now support for reporting generic CPU vulnerabilities to userspace, IP-triggered CPU backtracing, Svvptc extension, and the removal of the size limit on the XIP kernel.

### Miscellaneous Changes

Some other notable changes include:

* Initial support for the [Raspberry Pi 5](https://news.itsfoss.com/raspberry-pi-5/).
* Further enablement work for Intel's [CXL](https://en.wikipedia.org/wiki/Compute_Express_Link).
* Improved driver for Wacom drawing tablets.
* Enhanced KVM virtualization for LoongArch CPUs.
* Minor performance optimizations and fixes for Btrfs.
* Optional support for displaying a QR code (*Rust-based*) during kernel panic.

## Installing Linux Kernel 6.12

Users of [rolling release](https://itsfoss.com/rolling-release/) distributions will be among the first ones to receive this kernel release on their systems. Others, including the ones running LTS versions of a distribution, will have to wait before their distro offers it as part of a point release.

If you can't wait, then we have a [detailed guide](https://itsfoss.com/upgrade-linux-kernel-ubuntu/) on migrating to the latest mainline Linux kernel on Ubuntu. Back up your data before proceeding.

The tarball for Linux kernel 6.12 can be sourced from the [official website](https://www.kernel.org/).

<center>{% button "Linux Kernel 6.12" https://www.kernel.org/ %}</center>
