---
title: "反作弊：Linux 游戏玩家的棘手问题"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/11/anti-cheat-opinion-linux-gaming.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/11/anti-cheat-opinion-linux-gaming.png
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/anti-cheat-problem-linux-gamers/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

Linux 系统上的反作弊情况正日益恶化。让我们来看看你能做些什么。

<!-- more -->

得益于众多原生游戏的发布，以及像 [Wine](https://www.winehq.org/) 和 [Proton](https://github.com/ValveSoftware/Proton) 这类工具的出现，在 Linux 系统上玩游戏变得轻松愉快，原本为 Windows 系统开发的游戏也能在 Linux 上畅玩，如 [这篇文章](https://news.itsfoss.com/windows-game-on-linux-experience/) 所述。

遗憾的是，自 2023 年以来，多人游戏支持方面受到了重大打击，如 [这篇文章](https://news.itsfoss.com/roblox-linux-end/) 报道，2024 年下半年的情况也没有太大改善。许多 Linux 游戏玩家发现自己面临着新出现的兼容性问题，而这些问题在以前是不存在的。

你看，**许多热门游戏最近都削弱了对 Linux 的支持**。尽管它们一开始就没有正式支持该平台，但现在却让 Linux 游戏玩家更难与朋友一起享受多人游戏的乐趣了。

## 禁止 Linux 平台的游戏有哪些？

{% image https://news.itsfoss.com/content/images/2024/11/Anti_Cheats_Thorny_4_Linux_a.jpg '像《罗布乐思》《侠盗猎车手》和《Apex 英雄》等热门游戏最近是如何对待 Linux 游戏玩家的示意图。' %}

首先是艺电（EA），该公司掀起了一股反作弊热潮，为其热门游戏如 [《战地》](https://www.notebookcheck.net/Battlefield-1-burns-Steam-Deck-gamers-with-kernel-anti-cheat-in-new-update.905895.0.html)、《FIFA》和《模拟人生 4》等引入了 [EA 反作弊](https://help.ea.com/in/help/pc/ea-anticheat/) 解决方案，在此过程中却破坏了对 Linux 的支持。

他们在另一款游戏《Apex 英雄》上也采取了类似的做法，决定禁止 Linux 和 Steam Deck 用户玩这款游戏，[理由是作弊问题](https://news.itsfoss.com/apex-legends-drops-steam-deck/)。

别忘了 Rockstar Games，该公司为《GTA Online》实施了一个长期以来一直被呼吁的反作弊解决方案，但 [却完全忽略了 Linux 平台](https://news.itsfoss.com/linux-players-gta-v-support-dropped/)，未能为其启用支持。

## Linux 对游戏开发者来说是个问题吗？

当然，**有一些技术问题需要考虑**。与 Windows 不同，在 Linux 上使用内核级反作弊软件可能会是个大问题，因为用户可以完全控制内核，这使得检测作弊行为变得更加困难。

即便如此，像 BattlEye 和 Easy Anti-Cheat 这类反作弊软件 [确实原生支持 Linux](https://news.itsfoss.com/easy-anti-cheat-linux/)，所以游戏开发者和反作弊软件开发者都有改进的空间。

然而，在这一切中，有一点很明确：**游戏开发者不愿意给 Linux（作为一个平台）一个公平的机会**。一方面，他们坚称「[Linux 是作弊者的一扇敞开的门](https://r6fix.ubi.com/projects/RAINBOW6-SIEGE-LIVE/issues/LIVE-59642)」（*阅读置顶评论*），但另一方面，[Windows 上的作弊行为也十分猖獗](https://pure-oai.bham.ac.uk/ws/portalfiles/portal/238282817/checkmate24_collins_anti_cheat.pdf)（*研究论文*），针对任何受玩家欢迎的新老多人游戏，新的作弊手段都在不断涌现。

我们现在可没看到他们切断对 Windows 平台的支持，对吧？😑

是的，是的，**我知道 Windows 的市场份额比 Linux 大**，但仅仅因为一部分玩家使用基于 Linux 的操作系统，就将他们拒之门外，这难道不是有点不公平吗？难道不应该去追究作弊软件开发者的责任吗？

**考虑到运行 Linux 的 Steam Deck 用户数量**（*Linux 是其默认操作系统*），多人游戏开发者禁止 Linux 平台可能是搬起石头砸了自己的脚。

## 游戏开发者能做些什么？

{% image https://news.itsfoss.com/content/images/2024/11/Anti_Cheats_Thorny_4_Linux_b.jpg '' %}

首先，多为 Linux 游戏玩家考虑一下！玩家难道没有权利玩他们投入了时间和金钱的游戏吗？开发者只需要分配一些专门的时间和人力来处理 Linux 相关的问题，这将大有裨益。

但遗憾的是，**Linux 游戏玩家只是少数群体**，这些主流游戏开发者不太可能认真考虑 Linux 游戏玩家的需求。

最后，游戏开发者不应低估运行 Linux 的 Steam Deck 用户。随着 Steam Deck 等设备的出现，掌上游戏市场正在迎头赶上。

像 [Valve](https://www.valvesoftware.com/en/) 这样的公司都在投资 Linux 平台，忽视 Linux 可能不是一个明智的选择 😉

## 游戏玩家能做些什么？

{% image https://news.itsfoss.com/content/images/2024/11/Are_We_Anti-Cheat_Yet-.png '[「Are We Anti-Cheat Yet?」网站](https://areweanticheatyet.com/) 的截图。' %}

如果你想玩一款支持 Linux 且带有反作弊系统的多人游戏，我建议你浏览「[Are We Anti-Cheat Yet?](https://areweanticheatyet.com/)」网站。这是 **一个由社区驱动的资源网站**，包含了 1000 多款游戏的反作弊详细信息，每个条目都有有用的状态指示。

无论你是 Linux PC 游戏玩家还是 Steam Deck 用户，我都鼓励你支持像 [Supergiant Games](https://www.supergiantgames.com/)、[Klei Entertainment](https://www.klei.com/)、[Team17](https://www.team17.com/)、[Bitrich.info](https://store.steampowered.com/publisher/bitrich-info/) 等独立游戏开发者的游戏。

仅仅是因为他们愿意投入人力和时间，通过原生方式或借助 [Proton](https://github.com/ValveSoftware/Proton) 等工具为 Linux 提供支持。

我有没有遗漏其他支持 Linux 的优秀独立游戏开发者呢？欢迎在评论中提醒我 😉

你也可以选择玩这些热门的 PVP/PVE 游戏：

* [《军团要塞 2》](https://store.steampowered.com/app/440/Team_Fortress_2/)
* [《星露谷物语》](https://store.steampowered.com/app/413150/Stardew_Valley/)
* [《盖瑞模组》](https://store.steampowered.com/app/4000/Garrys_Mod/)
* [《泰拉瑞亚》](https://store.steampowered.com/app/105600/Terraria/)
* [《收获日 2》](https://store.steampowered.com/app/218620/PAYDAY_2/)
* [《求生之路 2》](https://store.steampowered.com/app/550/Left_4_Dead_2/)。

而且，如果你舍不得放弃一些在 Linux 上无法正常运行的游戏，最直接的解决办法就是 [在 Ubuntu 等发行版的基础上安装 Windows 形成双系统](https://itsfoss.com/install-ubuntu-1404-dual-boot-mode-windows-8-81-uefi/)，这样你就能两全其美了。

*💬 你怎么看？大型游戏开发者是在故意扼杀 Linux 上的多人游戏吗？*