---
title: Manjaro Linux Starts Experimenting With An Immutable Offering
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
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
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Manjaro Linux could become a more reliable option with immutability at its core. What do you think?

<!-- more -->

[Immutable Linux distributions](https://itsfoss.com/immutable-distro/) are a type of distro that are future-proof to quite some extent thanks to how they operate. In such systems, the core of the operating system is left untouched, with the root file system being read-only.

What this allows in is flexibility in handling updates, where a broken update wouldn't deem the operating system unrecoverable (*looking at you Ubuntu*). Some popular options include [NixOS](https://nixos.org/), [Vanilla OS](https://news.itsfoss.com/vanilla-os-2-orchid/), [Fedora Silverblue](https://fedoraproject.org/silverblue/), etc.

You can find more [immutable distro options](https://itsfoss.com/immutable-linux-distros/) in our list.

Of course, not everyone is a fan of such distros, with some believing that it's a gimmick.

This is where [Manjaro Linux](https://manjaro.org/) comes in, it's a community favorite [user-friendly Arch-based distro](https://itsfoss.com/arch-based-linux-distros/) that caters to a wide variety of use cases. Its developers have now dipped their toes into the immutable pond thanks to a recent announcement.

Let's see what they have been up to. 😃

{% note color:red 🚧 **Non-FOSS Warning!** This is an under-development Linux distro, general use or production use is not recommended. %}

## Manjaro Immutable: What to Expect?

![a screenshot of an early testing version of manjaro immutable](https://static.fosscope.com/articles_img/2024/08/manjaro-linux-starts-experimenting-with-an-immutable-offering/Manjaro_Immutable_Testing.jpg)

Introduced as **a community testing release**, Manjaro Immutable is powered by [Arkdep](https://github.com/arkanelinux/arkdep), the popular toolkit for creating immutable btrfs-based systems, and [Arkane Linux](https://news.itsfoss.com/arkane-linux/), an “*opinionated, immutable, atomic, multi-root Arch-based distribution*”.

As this is **an experimental release**, the developers of Manjaro hope to collect feedback from the community to see how the tech underneath Manjaro Immutable fares in day-to-day use. Do keep in mind that this doesn't guarantee a full release someday.

When [asked](https://forum.manjaro.org/t/manjaro-immutable-out-now-for-community-testing/166364/2) by a community member **whether this would become an official variant for Manjaro**, [Roman Gilg](https://www.linkedin.com/in/roman-gilg/), CTO at Manjaro Linux said that:

> Our plan is definitely for it to become an official variant of Manjaro. With the community testing version we’re now gathering some feedback on what people expect from such a variant and what should still go in there or what could be slimmed down.

There was also [a question](https://forum.manjaro.org/t/manjaro-immutable-out-now-for-community-testing/166364/14) asking **whether an ARM version was planned**.

To that, Manjaro developer [Dennis ten Hoove](https://github.com/dennis1248) added that it would be possible. However, it's untested, and nothing is planned as of now. But, they might try something in the future.

## 📥 Get Manjaro Immutable

You can get the community testing ISO from the official [download mirror](https://download.manjaro.org/manjaro-gnome-immutable/20240801/manjaro-gnome-immutable-2024.08.01-x86_64.iso).

You can either install it on bare metal, or opt for running it on a [virtual machine](https://itsfoss.com/virtual-machine/) using VirtualBox or QEMU. Do remember that **enabling EFI is mandatory**, and a minimum 32 GB of storage is required to install the thing.

<center>{% button "Manjaro Immutable (direct download)" https://download.manjaro.org/manjaro-gnome-immutable/20240801/manjaro-gnome-immutable-2024.08.01-x86_64.iso %}</center>

Users who want to go the extra mile can **provide feedback to the developers** by joining the dedicated [Matrix channel](https://matrix.to/#/%23Manjaro-Immutable:matrix.org) for it, or by replying to the [initial announcement](https://forum.manjaro.org/t/manjaro-immutable-out-now-for-community-testing/166364) on the Manjaro forum.

*💬 Are you looking forward to using an immutable Manjaro? Let me know below!*
