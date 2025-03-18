---
title: 我与原生 Linux 游戏的 30 天实验
date: 2024-09-23 09:21:40
author:
  - fosscope-translation-team
  - 2024zht
  - excniesnied
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/linux-gaming-review.webp
cover: https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/linux-gaming-review.webp
categories:
  - 翻译
  - 新闻
tags: 
  - Linux
  - 游戏
authorInfo: |
  via: https://news.itsfoss.com/native-linux-game-experience/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[2024zht](https://github.com/2024zht)
  校对：[excniesNIED](https://github.com/excniesNIED) [Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

在 Linux 系统上测试 Steam 支持的游戏。以下是测试过程。

<!-- more -->

自从我那台装有 Windows 的游戏 PC 因为电源供应单元（PSU）烧坏而无法使用后（并非因为 Windows 系统😆），过去几周我一直在我的装有 Ubuntu 的笔记本电脑上玩游戏。

令人惊讶的是，体验一直 [相当不错](https://news.itsfoss.com/windows-game-on-linux-experience/)，无论是非原生游戏还是原生游戏都运行良好。当然，我也确实遇到了一些问题，但同时也度过了许多愉快的时光！

那么，就跟随我一起了解我在 Linux 上玩原生游戏的经验吧。

## 原生 Linux 游戏：应该让更多人知道这个！

![an illustration with a penguin and gamepad with a blue green background having a prism pattern](https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/Native_Linux_Games_a.webp)

本文中，我将展示三款通过官方 Steam 客户端（*.deb*）为 Linux 安装的流行原生游戏。 测试系统的规格如下：

- **机型：** Dell G15 5530
- **RAM：** 16 GB
- **CPU：** Intel Core i5-13450HX
- **GPU：** NVIDIA GeForce RTX 3050 6 GB
- **显示器：** 15.6", FHD 1920×1080, 120Hz & 24" FHD 1920×1080, 60 Hz
- **驱动：** NVIDIA 535.183.01
- **操作系统：** Ubuntu 22.04.4 LTS
- **电源模式：** 平衡
- **桌面环境：** GNOME 42.9
- **会话：** X11
- **模组：** 无

## 反恐精英 2

我们从广受欢迎的 [《反恐精英 2》](https://store.steampowered.com/app/730/CounterStrike_2/) 开始，这是知名游戏《CS:GO》的续作。为了保持 120 帧的稳定帧率（这是我笔记本电脑内置显示器支持的最高帧率），我不得不调整了一些图形设置，主要是介于中等或高之间。

![a screenshot of counter strike 2 running on ubuntu 22.04.4 lts](https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/Native_Linux_Games_b.jpg)

我尝试了多种游戏模式，如休闲模式、死亡竞赛、军备竞赛、竞技模式，以及我最喜欢的 Premier 模式。在几乎所有这些比赛中，我都能获得流畅的 120 帧体验，没有任何音视频问题。

但是，还有一些其他奇怪的问题。偶尔，游戏会突然崩溃，没有错误代码或任何提示，前一秒游戏还在正常运行，下一秒我就只能盯着桌面的壁纸发呆。

另一个问题是当我连接了外部显示器时。每当我尝试将游戏拖动到更快的笔记本电脑屏幕上时，游戏拒绝最大化，我必须点击任务栏中的游戏图标才能使它回到前台。

同样的情况有时也会发生在仅使用笔记本电脑的显示器时，为了解决这个问题，通常通过使用 {% kbd Alt %} + {% kbd Tab %} 在应用程序之间切换就能解决。

## 美国卡车模拟器

另一款我玩过的游戏是 [《美国卡车模拟器》](https://store.steampowered.com/app/270880/American_Truck_Simulator/)，如果你看过我定期更新的 [最佳 Steam 特卖游戏](https://news.itsfoss.com/best-steam-games-linux-sale/) 列表，你可能知道我喜欢玩模拟游戏。

![a screenshot of american truck simulator running on ubuntu 22.04.4 lts](https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/Native_Linux_Games_c.jpg)

尽管它的姐妹游戏 [《欧洲卡车模拟器 2》](https://store.steampowered.com/app/227300/Euro_Truck_Simulator_2/) 是我个人在这两款游戏中的最爱，但《美国卡车模拟器》在我用 Linux 玩的时候也表现得相当不错。

我进行了一些长途旅行，从美国的西南部到西北部，我从未遇到过任何崩溃问题，而我的彼得比尔特卡车，却经历了不少事情。☠️

[《卡车世界》](https://www.worldoftrucks.com/) 的整合功能如预期般工作，我也能够从我旧的职业存档中继续游戏。

甚至网络电台也按预期工作，让我能够在巡航标志性的路线时，调谐到一些现实生活中的美国广播频道。遗憾的是，这个游戏也有一些问题。

上面这张照片，你注意到它看起来有多么褪色和明亮吗？

当我使用游戏内的拍照模式（该模式也与 Steam 的截图工具绑定）时，结果就是这样，而且要明确的是，由于游戏中的雨天天气，游戏世界是阴暗和阴沉的。

但情况变得更糟了。👇

![a screenshot of american truck simulator running on ubuntu 22.04.4 lts](https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/Native_Linux_Games_d.jpg)

原始图像的方向是错误的，并且是镜像的，我不得不使用 [Shotwell](https://shotwell-project.org/doc/html/) 进行编辑，然后才将其添加到文章中。在 Steam 社区中也有 [一份报告](https://steamcommunity.com/app/270880/discussions/0/4554911223882789939/)，另一位用户遇到了类似的问题。我真心希望 [SCS 软件公司](https://www.scssoft.com/) 能修复导致这一问题的任何原因。

我遇到的另一个问题是无法在游戏窗口外使用鼠标光标。即使在游戏中，{% kbd Super %} 键也不起作用，幸运的是，我可以通过 {% kbd Alt %} + {% kbd Tab %} 切换，但没有鼠标光标，我回到了方标。

需要注意的是，上述问题在内部笔记本电脑显示器和连接外部 60 Hz 显示器时都发生了。

## 铁路调度模拟器

![a screenshot of rail route running on ubuntu 22.04.4 lts](https://static.fosscope.com/articles_img/2024/08/my-30-day-experiment-with-native-linux-games/Native_Linux_Games_e.jpg)

在本文提到的游戏中，[《铁路调度模拟器》](https://store.steampowered.com/app/1124180/Rail_Route/)无疑是**表现最佳**的，它从未崩溃，在我更改工作区或显示器时也没有出现任何异常行为，窗口切换更是轻松自如。

如你所见，我能够在高峰时段游戏模式中管理一个庞大的客运和货运网络。这既有趣又具有挑战性。

## 我的想法

尽管我遇到了一些问题，但我仍然每天在我的 Linux 电脑上玩游戏。我相信随着时间的推移，游戏体验会越来越好，特别是如果越来越多的人开始在 Linux 上玩游戏。这样，开发者可以收到准确的报告来修复问题，这应该间接地帮助其他非原生游戏。

*💭 你对 Linux 游戏体验有何看法？你在 Linux 系统上玩什么游戏？*
