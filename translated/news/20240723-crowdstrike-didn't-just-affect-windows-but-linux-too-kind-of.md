---
title: CrowdStrike 不仅影响 Windows，还影响 Linux！ (某种程度上）
date: {{release_date}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/crowdstrike-didn't-just-affect-windows-but-linux-too-kind-of/crowdstrike-affects-linux-users.webp
cover: https://static.fosscope.com/articles_img/2024/08/crowdstrike-didn't-just-affect-windows-but-linux-too-kind-of/crowdstrike-affects-linux-users.webp
categories:
  - 翻译
  - 新闻
tags: 
  - CrowdStrike
authorInfo: |
  via: https://news.itsfoss.com/crowdstrike-windows-linux/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

CrowdStrike 无处不在地造成破坏！

<!-- more -->

上周末，由于总部位于德克萨斯州奥斯汀的网络安全公司 [CrowdStrike](https://www.crowdstrike.com/) 向 Windows 推送了一个错误补丁，IT 行业发生了一起灾难性事件。

尽管如此，对于那些想早点下班的人来说，这个时间点可能是个福音。

许多重要的基础设施，如机场和医疗设施首当其冲，**这引发了许多关于是否依赖此类集中式技术的重要问题**。

幸运的是，这个问题后来 [得到了解决](https://www.crowdstrike.com/falcon-content-update-remediation-and-guidance-hub/)，但这并没有阻止包括我们在内的许多人就 CrowdStrike 的困境制作一些 [有趣的梗图](https://x.com/itsfoss2/status/1814314761254838419)。 

遗憾的是，在这次灾难性事件发生前几周，Linux 也受到了 Crowdstrike 的影响，但这一事件在很大程度上不为人知，直到现在才被人知晓。🫤

## CrowdStrike 的无能： 次等待遇的沉重代价

![a screenshot of a forum post on rocky linux forums outlining an issue with crowdstrike falcon](https://static.fosscope.com/articles_img/2024/08/crowdstrike-didn't-just-affect-windows-but-linux-too-kind-of/CrowdStrike_Linux_Booboo_a.webp)

今年5月，一位 Rocky Linux 用户在论坛上发布 [issue](https://forums.rockylinux.org/t/crowdstrike-freezing-rockylinux-after-9-4-upgrade/14041) 称，在配备 CrowdStrike [Falcon 平台 ](https://www.crowdstrike.com/platform/) 的服务器上升级到 [Rocky Linux 9.4](https://rockylinux.org/news/rocky-linux-9-4-ga-release) 会导致系统因 [内核错误](https://en.wikipedia.org/wiki/Kernel_panic) 而崩溃。

**他用户也纷纷反映遇到类似问题**，在四处寻找可能的修复方法后，他们终于在 Red Hat 的客户门户网站上找到了一个修复方法。

在 [Hacker News](https://news.ycombinator.com/item?id=41005936&) 上，另一位深受 CrowdStrike 无能之苦的用户分享说，当 CrowdStrike 为 Debian 稳定版推送了一个不兼容的补丁时，，一批运行 [Debian](https://www.debian.org/) 的生产机器被迫下线。

当他们最初联系支持人员时，CrowdStrike 花了一天时间才做出回应，然后要求提供更多的证据（除了已经提供的证据），他们又花了几天时间才承认问题。 

在让他们等待了几个星期后，CrowdStrike 发送了一份根本原因分析，其中提到他们不支持 Debian 稳定版运行 N-1 版本的特定场景，而用户认为这是一种受支持的配置。

### **但是，等等，还有更多！**

![a screenshot of red hat customer portal article outlining an issue with cloudflare falcon](https://static.fosscope.com/articles_img/2024/08/crowdstrike-didn't-just-affect-windows-but-linux-too-kind-of/CrowdStrike_Linux_Booboo_b.webp)

类似情况，**许多 Red Hat Enterprise Linux (RHEL) 用户也面临着 Falcon 带来的问题**，为此 Red Hat 不得不发布多个警告。

[第一种情况](https://access.redhat.com/solutions/7068083)（仅限订阅者）是我之前提到的 Rocky Linux，在 Linux 内核 5.14.0-410 及更高版本的系统上，由于 falcon-sensor 进程的原因，启动后会出现内核错误。

[第二种情况](https://access.redhat.com/solutions/6971903) 是 RHEL 6 和 7 上的系统崩溃问题，Red Hat 提供了一种解决方法，建议用户禁用 Falcon 以缓解问题，另一种方法是联系 CrowdStrike 支持部门寻求帮助。

*现在，我们知道 CrowdStrike 的客户服务有多及时了。 ☠️*

不出所料，由于这场混乱，美国众议院 [国土安全委员会](https://homeland.house.gov/) 已正式致函 CrowdStrike 首席执行官 [George Kurtz](https://www.linkedin.com/in/georgekurtz)，要求他就此次大规模故障作证。

我本以为这是因为基于 Linux 的操作系统受到了影响，但众所周知，[Windows](https://www.microsoft.com/en-us/windows/) 是大多数人最喜欢的操作系统。

有趣（或不祥！？）的事实是，George 在 2010 年担任 McAfee 的首席技术官（CTO）时，那次臭名昭著的 [DAT 5958](https://en.wikipedia.org/wiki/McAfee#DAT_5958_update) 杀毒软件更新导致全球数百万台装有 Windows 的计算机瘫痪。

*💬 CrowdStrike 为梅赛德斯-AMG PETRONAS [F1 车队](https://www.mercedesamgf1.com/) 提供赞助和基础设施支持，因此我这个赛车迷对 CrowdStrike 有所了解。 你呢？在这之前你听说过他们吗？*
