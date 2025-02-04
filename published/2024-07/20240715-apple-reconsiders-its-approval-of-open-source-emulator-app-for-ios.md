---
title: 苹果公司重新考虑批准 iOS 的开源模拟器应用程序
date: 2024-07-31 6:23:12
abbrlink: 20240715-apple-reconsiders-its-approval-of-open-source-emulator-app-for-ios
author:
  - fosscope-translation-team
  - excniesNIED
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2024/07/apple-reconsiders-its-approval-of-open-source-emulator-app-for-ios/apple-reconsiders-opensource-emulation.webp
cover: https://static.fosscope.com/articles_img/2024/07/apple-reconsiders-its-approval-of-open-source-emulator-app-for-ios/apple-reconsiders-opensource-emulation.webp
categories:
  - 翻译
  - 新闻
tags: 
  - UTM SE
  - iOS
  - 模拟器
authorInfo: |
  via: https://news.itsfoss.com/apple-approves-utm-se/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

感谢苹果公司为用户提供更多开源选择！

<!-- more -->

如果每次 [苹果公司](https://www.apple.com/) 为了「保护其生态系统」而采取措施时我都能得到一毛钱，那我现在早就成富翁了😁

就在大约一个月前，他们决定 [阻止一款开源 iOS 模拟器应用发布](https://news.itsfoss.com/apple-blocks-utm-se/)，却没有明确说明问题所在。

就连开发者也放弃了，称 UTM SE 是一种 *「糟糕的体验，不值得为之奋斗」* ，除非苹果公司改变立场，否则他们不会在这上面投入更多的时间和精力。

然而，出人意料的是，苹果公司撤销了最初基于「保护生态系统」的决定，这一举动颇为罕见。

## 苹果公司对 UTM SE 的态度变化：有何进展？

> 我们很高兴地宣布 UTM SE 可在 iOS 和 visionOS 的 App Store 上（免费）使用（并且即将在 AltStore PAL 上推出）！ 
> 
> 感谢 AltStore 团队的帮助，并感谢苹果公司重新考虑他们的政策。
>
> — UTM (@UTMapp) [2024 年 7 月 13 日](https://twitter.com/UTMapp/status/1812238024220238180)

上周末，UTM [宣布](https://x.com/UTMapp/status/1812238024220238180) UTM SE 现已支持 iOS 和 visionOS，并感谢 [AltStore](https://altstore.io/) 团队为他们提供了帮助，同时对苹果公司重新审视其政策表示感谢。

如果你不熟悉，UTM SE 是 [UTM](https://getutm.app/) 的简化版。一个运行在苹果公司设备上的模拟器/虚拟机，允许用户在他们的设备上运行不同的操作系统。

一些**主要功能**包括：

- **基于 QEMU**
- **虚拟机可自定义配置**
- **支持模拟 x86、RISC-V 和 PPC**
- **图形化的 VGA 模式和纯文本的终端模式**

尽管如此，用它模拟旧版操作系统的体验应该还不错，但不要指望它能以很高的性能完整运行 Ubuntu 或 Fedora 等现代 Linux 发行版。

这是因为缺乏 [JIT（即时编译）](https://en.wikipedia.org/wiki/Just-in-time_compilation) 支持，苹果公司仍然以 *「安全原因」* 为由对此严加防范并加以封锁。但问题是，安卓系统早就支持 JIT 了。

当然，我，[福尔摩斯](https://en.wikipedia.org/wiki/Sherlock_Holmes)，认为，苹果公司只是不想被人发现自己的不足，试图绕过 [《数字市场法案》（DMA）](https://digital-markets-act.ec.europa.eu/index_en) 罢了。 就拿 [Epic Games 诉苹果公司案](https://en.wikipedia.org/wiki/Epic_Games_v._Apple) 来说吧，苹果公司在**两次**拒绝后，最终 [批准了](https://arstechnica.com/gadgets/2024/07/report-apple-approves-epic-games-store-on-ios-in-europe/) Epic Games 商店应用在欧洲 iOS 上的发布

*我还是认为，苹果公司不到被迫的时候是不会真正学习的。* 😆

## 📥 获取 UTM SE

目前，用户可在 [App Store](https://apps.apple.com/us/app/utm-se-retro-pc-emulator/id1564628856) 下载 UTM SE。该应用已对 **iPhone**、**iPad** 和 **Apple Vision** 开放。

<center>{% button "UTM SE (App Store)" https://apps.apple.com/us/app/utm-se-retro-pc-emulator/id1564628856 %}</center>

如上文所述，开发人员还提到 UTM SE 将很快登陆 [AltStore PAL](https://rileytestut.com/blog/2024/04/17/introducing-altstore-pal/)，一家面向欧洲用户的开源和去中心化的应用商店。

*💬 你如何看待苹果公司的决定？他们是想避免 DMA 的合规性问题吗？*
