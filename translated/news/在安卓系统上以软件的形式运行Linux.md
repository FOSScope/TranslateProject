---
title: <在安卓系统上以软件的形式运行 Linux>
date: <2024-06-22>
author:
  - fosscope-translation-team
  - <Fisherman110>
  - <void-mori>
banner: <https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/06/run-linux-in-android.png>
cover: <https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/06/run-linux-in-android.png>
categories:
  - 翻译
  - <news>
tags:
  - <news>
authorInfo: |
  via: <https://news.itsfoss.com/lindroid/>

  作者：[<Sourav Rudra>](<https://news.itsfoss.com/author/sourav/>)
  选题：[<Cubik65536>](https://github.com/Cubik65536)
  译者：[<Fisherman110>](https://github.com/Fisherman110)
  校对：[<void-mori>](https://github.com/void-mori)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

<!-- 所有在被 `<>` 标记的地方都需要被替换成对应的内容 -->

## Linux 能够以各种形式和规模运行，这是毋庸置疑的

<!-- more -->

毫无疑问，安卓是世界上最流行的开源操作系统。（对不住了，arch 用户）安卓使用高度定制的 Linux 内核给用户提供了良好的智能手机使用体验。

当然，并非每个人都喜欢谷歌概念下的安卓操作系统，他们还有 LineageOS, CalyxOS 等谷歌系列以外的系统可以选择。

然而，在最近的一份声明中。Erfan Abdi 和 Luka Panio 两位开发者介绍了一个叫做 Lindroid 的有趣项目。这个项目致力于让用户可以在安卓设备上用一种新方式运行Linux。

## Lindroid项目：有哪些东西值得期待？

![小米6平板上通过lindroid运行debian12的截图](https://news.itsfoss.com/content/images/size/w1000/2024/06/Lindroid_a.jpeg)

通过这个项目，用户可以在他们的安卓系统上使用本地硬件运行各式各样的 Linux 发行版 。开发者 Erfan 称呼这个项目为：“逆向安卓模拟器”（即在安卓模拟 PC 操作系统）

如上图所示，Debian12运行在一个安装了 LineageOS 的小米6平板上，这体现了 Lindroid可以毫不费力地在本地硬件上运行各种 Linux 发行版。

Lindroid 默认的图形界面是 KWin,Wayland 默认启用，对 X11 的支持还在实验阶段。

在项目启动的时候，Erfan提到：

    我个人的目标是让所有人更轻松地使用 Linux,我期待未来有更多的人热爱 Linux 移动版本社区，参与 Linux 移动版本社区的贡献开发。🙏🙏

他也展示了许多令人印像深刻的 Lindroid 特性。比如说多源输入和多屏显示支持。

![展示 Lindroid 的多屏显示和多源输入特性的视频](https://news.itsfoss.com/content/images/2024/06/Lindroid_b.gif)

这个视频展示了切屏显示是毫不费力的，移动过程中毫无延迟。他补充道，这项功能和安卓的多屏模式是适配的，多屏模式在即将到来的安卓15发布版中会得到改进。

你可能会好奇，在 Lindroid 运行软件是否可行？

开发者通过实现硬件加速确保了它（Lindroid）在运行软件方面也毫不逊色。这是通过使用 libhybris 库来调用宿主机的 EGL 和硬件混合渲染来实现的。

当被问到 Wine 能否在这上面运行的时候， Erfan补充道，他还没有测试 Wine,但是他继续不久之后进行测试，他会尝试建立 GL(存疑？)来确保 Wine 和 Proton 的适配性。

他也展示了 Lindroid 在类似 Ubuntu Touch (Lomiri), Droidian (Phosh), 和 Plasma Mobile 这样的发行版上面运行的情况。

如果你迫切想要了解更多关于这个炫酷项目的信息，你可以去 X（twitter)频道寻找信息，或者参考 Luka 在Volla Community Days的演说(4:01:00 timestamp)，他在这场演说中回答了很多观众提出的有趣问题。

## 想要上手此项目？

在你开始之前，你需要一个获得 root 权限，包含一些 AOSP 补丁的安卓设备来运行 Lindroid。在没有 root权限的设备上运行 Lindroid是不可行的，因为它的底层架构使用了 LXC 来连接宿主机的驱动。

不过，还有一个问题。目前，还没有开箱即用的办法来运行 Lindroid, Erfan提到过部署配置 Lindroid并不容易。但是，他很快就会做出一份公开教程。

值得一提的是，他宣布 Lindroid 将会正式在 LibreMobileOS 上以 Ulumo 之名上线，它的特性是有一个 Ubuntu实例。

我期待那（Ulumo)会是一个安装后就不用管理的省心 Lindroid 解决方案。此外，他在这方面（Ulumo)没有发表其他看法了。

如果你想要参与开发或者了解工程进度的话，你可以访问这个工程的 GitHub 页面。

[Lindroid(GitHub)](https://github.com/linux-on-droid/)                                                                     
