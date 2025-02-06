---
title: Linux 家用服务器能做的 7 件神奇之事
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/linux-home-server.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/linux-home-server.png
categories:
  - 翻译
  - 技术
tags: 
  - 清单
authorInfo: |
  via: https://itsfoss.com/homelab-usage

  作者：[Community](https://itsfoss.com/author/community/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

你 Linux 家用服务器的功能比你想象的还要强大！

<!-- more -->

Linux 几乎可以在任何地方运行。要是有设备不能运行 Linux，那也总有办法让它运行起来😉

而 Linux 最实用的应用场景之一便是搭建家用服务器。当然，你也可以用 Windows 来搭建家用服务器，但从长远来看，Linux 会是更可靠的选择。在本文中，我将列举 Linux 家用服务器的多种用途，希望能够说服在你今天就搭建属于自己的服务器。

## 什么是 Linux 家用服务器？

家用服务器是一种本地托管的私有服务器，可通过家庭网络或互联网进行访问。而在这种情况下，它由 Linux 系统提供支持。拥有 Linux 家用服务器的主要优势之一在于，你能够完全掌控自己的数据，并保障媒体串流活动的隐私安全。

有时，Linux 家用服务器也被称为家庭实验室（通过这篇文章，你可以了解更多相关信息）：

{% link https://linuxhandbook.com/homelab/ 什么是家庭实验室，你为什么需要一个？ icon:https://linuxhandbook.com/content/images/2021/11/homelab-setup.webp %}

有众多可供选择的开源软件，它们能让你的家用服务器满足特定的使用需求。例如，Plex 或 Kodi 可作为媒体服务器，Samba 可用于共享文件，Nextcloud 可用于文件协作与同步。

搭建家用服务器超出了本文的讨论范围。不过，使用 Ubuntu 作为 Linux 发行版来驱动你的硬件是个稳妥的选择。

完成系统安装后，你需要从众多适用于家用服务器的开源免费软件中进行挑选，然后就可以开始使用了。

既然我们已经了解了什么是 Linux 家用服务器，那它具体有哪些用途呢？下面我来重点介绍一些：

## 1. 搭建私人云存储

![linux 家用服务器云存储](https://itsfoss.com/content/images/2024/07/cloud-storage-linux-home-server.png)

**文件存储**或许是 Linux 家用服务器最广泛使用的功能，它能让你存储和共享文件、文档、照片、视频等。此外，由于这是你自己的云服务器，不存在隐私风险。

当然，你需要负责文件备份或设置 RAID 阵列。因此，你需要投入大量时间学习相关技术，以确保文件安全。

你可以在全球任何地方、使用任何设备访问你的 Linux 云服务器。这意味着只需敲几下键盘，你就能连接到自己的服务器。

Nextcloud 是一款理想的开源应用程序，可帮助你搭建属于自己的云服务器。

## 2. 智能家居控制

拥有一个能控制所有智能家居设备的遥控器，这是每个人都梦寐以求的。而借助 Linux 家用服务器，这个梦想可以成为现实。

通过 Linux 服务器，你可以为所有家用设备创建一个控制中心，比如恒温器、智能灯泡、闭路电视摄像头、智能风扇、空调以及所有联网设备。

有各种家庭自动化软件，如 [Home Assistant](https://github.com/home-assistant/home-assistant)，你可以对其进行配置以实现这一功能。

## 3. 媒体服务器

![Linux 家用服务器媒体服务器](https://itsfoss.com/content/images/2024/07/media-server-linux-home-server.png)

既然可以将媒体文件放在 Linux 家用服务器上，何必还要费力地在所有设备间共享这些文件呢？你也可以告别流媒体服务，随时观看自己喜欢的节目。

像 Jellyfin 这样的软件可以帮你搭建一个强大的本地媒体流解决方案。你可以通过家庭网络或互联网（需要进行高级配置）访问它。

{% link https://itsfoss.com/jellyfin-raspberry-pi/ 在树莓派上搭建 Jellyfin 媒体服务器 icon:https://itsfoss.com/content/images/2024/03/setup-jellyfin-media-server-on-raspberry-pi5.png %}

## 4. 网络安全、广告拦截或监控

![Linux 家用服务器网络](https://itsfoss.com/content/images/2024/07/network-linux-home-server.png)

如果你知道如何操作，就可以使用 Linux 家用服务器运行网络安全软件或监控你的设备和网络。

即使你不是网络安全爱好者，也可以安装一款名为 Pi-hole 的流行开源软件来拦截广告和追踪器。此外，像 Shorewall 这样的软件可以帮助你创建防火墙。

总之，你可以利用 Linux 家用服务器保护你的设备免受恶意软件和安全漏洞的侵害。

{% link https://itsfoss.com/setup-pi-hole/ 如何设置 Pi-hole，享受无广告生活 icon:https://itsfoss.com/content/images/wordpress/2022/11/install-pi-hole.png %}

## 5. 开发与测试

如果你是一名开发者，Linux 家用服务器对你来说简直就是天堂。借助众多测试环境和数据库主机，Linux 服务器能让你创建出最佳模型。

正如我在引言部分提到的，我们也将家用服务器称为家庭实验室。你可以随意使用这两个术语，但我认为当你进行测试工具、学习和开发相关工作时，使用“家庭实验室”这个术语更为准确。

如果你对此感兴趣，我们还有一篇相关指南可以帮助你入门：

{% link https://itsfoss.com/zimaboard-review/ ZimaBoard 让我拥有家庭实验室的梦想成真 icon:https://itsfoss.com/content/images/2024/03/zimabord-review.png %}

## 6. 游戏托管

![Linux 游戏服务器](https://itsfoss.com/content/images/2024/07/game-linux-home-server.png)

Linux 家用服务器能满足每个人的需求。如果你是一名游戏玩家，Linux 服务器完全可以用来托管私人多人游戏服务器。

你既可以为个人使用创建自己的游戏服务器，也可以搭建一个商业游戏服务器来赚钱（比如反恐精英服务器）。

自定义游戏服务器可以让你定制多人游戏体验。如果你知道自己在做什么，这将是一次有趣的体验。

## 7. 打印服务器

Linux 家用服务器可以充当集中式打印管理平台，帮助你跟踪所有打印任务。

借助 Linux 服务器，你可以实现各种共享打印功能，不同设备可以使用同一台打印机。此外，一台 Linux 家用服务器可以同时管理多台打印机，而不仅仅是一台。

当然，只有在你拥有类似小型办公室那样配备多台打印机的环境中，这才是一个可行的应用场景。但这确实是一个很有趣的用途。

## 总结

你可以创造性地利用家用服务器。无论是想存储文件、搭建家庭自动化解决方案，还是设置安全工具，Linux 家用服务器都是不错的选择。

它总有办法满足你的需求，而且成本效益很高。不过，搭建和维护它需要一定的技术知识。

*💭 我是否遗漏了你最喜欢的 Linux 家用服务器使用方式？欢迎在下方评论区告诉我！*