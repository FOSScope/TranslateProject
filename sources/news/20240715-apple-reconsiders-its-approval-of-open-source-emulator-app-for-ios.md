---
title: Apple Reconsiders its Approval of Open-Source Emulator App for iOS
date: {{release_date}}
author:
  - fosscope-translation-team
  - excniesNIED
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/apple-reconsiders-opensource-emulation.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/apple-reconsiders-opensource-emulation.png
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/apple-approves-utm-se/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

Thank you, Apple, more open-source options for the users!

<!-- more -->

If I got a dime each time [Apple](https://www.apple.com/) did something to gatekeep their ecosystem, I would've been a wealthy man by now 😁

Just a month or so ago, they had decided to [block the publishing](https://news.itsfoss.com/apple-blocks-utm-se/) of an open-source emulator app for iOS, without providing any clarity over what the issue was.

Even the developers gave up, citing that UTM SE was a “*subpar experience and isn't worth fighting for*”, and unless Apple changed their stance, they wouldn't invest any additional time/effort into it.

But, in a surprise move, Apple has gone back on the initial gatekeeping-fueled decision, which is unusual to see.

## Apple Warms Up To UTM SE: What Gives?

> We are happy to announce that UTM SE is available (for free) on iOS and visionOS App Store (and coming soon to AltStore PAL)!  
>
> Shoutouts to AltStore team for their help and to Apple for reconsidering their policy.[https://t.co/HAV5JnT5GO](https://t.co/HAV5JnT5GO)
>
> — UTM (@UTMapp) [July 13, 2024](https://twitter.com/UTMapp/status/1812238024220238180?ref_src&#x3D;twsrc%5Etfw&amp;ref&#x3D;news.itsfoss.com)

Over the weekend, UTM [announced](https://x.com/UTMapp/status/1812238024220238180) that UTM SE was now available for iOS and visionOS, and that the [AltStore](https://altstore.io/) team helped them out, with a thanks to Apple for revisiting their policy.

If you are not familiar, UTM SE is the less powerful version of [UTM](https://getutm.app/), an emulator/virtual machine host for Apple devices that allows users to run different operating systems on their machines.

Some **key features** include:

- **Based on QEMU**
- **Custom Configs for Machines**
- **Support for emulating x86, RISC-V, and PPC.**
- **VGA Mode for Graphics & Terminal Mode for Text-Only**

Having said that, the emulation experience for old operating systems with this should be decent, but, don't expect anything extraordinary like running a modern Linux distro such as Ubuntu or Fedora in their full glory, with usable performance.

That is thanks to the lack of [JIT](https://en.wikipedia.org/wiki/Just-in-time_compilation) support, which Apple still closely guards, keeping it locked up, citing “*security reasons*”. Here's the catch, though, Android has had that support for ages now.

Naturally, the [Sherlock Holmes](https://en.wikipedia.org/wiki/Sherlock_Holmes) in me thinks that Apple just doesn't want to be caught lacking, trying to skirt their way around the [Digital Markets Act](https://digital-markets-act.ec.europa.eu/index_en) (DMA). Take [the battle](https://en.wikipedia.org/wiki/Epic_Games_v._Apple) between them and Epic Games, which has seen them finally [approve](https://arstechnica.com/gadgets/2024/07/report-apple-approves-epic-games-store-on-ios-in-europe/) the Epic Games store app for iOS in Europe, after they rejected it **twice**.

*I still think that Apple doesn't really learn until it is forced to.* 😆

## 📥 Get UTM SE

For now, those who are interested in trying UTM SE out can get it from the [App Store](https://apps.apple.com/us/app/utm-se-retro-pc-emulator/id1564628856), where it has been made available for the **iPhone**, **iPad**, and **Apple Vision**.

[UTM SE (App Store)](https://apps.apple.com/us/app/utm-se-retro-pc-emulator/id1564628856)

The developers have also mentioned that UTM SE will be arriving at [AltStore PAL](https://rileytestut.com/blog/2024/04/17/introducing-altstore-pal/) very soon (*as mentioned in the tweet above*). It is a store geared towards European users, which is open-source and decentralized in nature.

*💬 What do you think of Apple's decision? Are they trying to avoid a compliance issue with DMA?*
