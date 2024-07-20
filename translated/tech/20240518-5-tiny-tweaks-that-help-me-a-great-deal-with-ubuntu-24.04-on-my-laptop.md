---
title: 5 个细微的调整,帮助我在笔记本电脑上使用 Ubuntu 24.04
date: <发布时间>
author:
  - fosscope-translation-team
  - Betty-hub182
  - <校对者ID>
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/05/ubuntu-laptop-tiny-tweaks.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/05/ubuntu-laptop-tiny-tweaks.png
categories:
  - 翻译
  - 技术
tags:
  - Ubuntu
authorInfo: |-
  via: https://itsfoss.com/ubuntu-tweaks-for-laptop/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesnied](https://github.com/excniesNIED)
  译者：[Betty-hub182](https://github.com/Betty-hub182)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

我在笔记本电脑上运行 Ubuntu 时做了一些简单的调整和设置更改。

<!-- more -->

让我分享一些帮助我在笔记本电脑上更顺畅地运行 Ubuntu 的调整。

这是基于我的偏好，您可能不一定要进行相同的更改。此外，这些都不是开创性的，从未见过的技巧。

我将分享我在笔记本电脑上使用 Ubuntu 时所做的一些简单的改变。

并且这些技巧并不是针对 Ubuntu 24.04 的。你也可以在其他 Ubuntu 版本中找到它们。

## 启用轻敲以点击

传统上，触控板底部有左键和右键按钮。我认为这是由于人们更习惯于鼠标的左键和右键。

但是随着时间的推移，这种行为发生了变化，因为像你我这样的用户更习惯于轻敲触控板进行点击。 **一根手指点击左键，两根手指点击右键**。

笔记本电脑制造商已经意识到了这种行为的变化，如今，你很难在触控板上看到专用的左键和右键。对了，你仍然可以转到底部，按下它进行左键和右键操作。

然而，我更习惯 「轻敲以点击」 的行为。我觉得这样更方便。

该功能可以从触控板设置中启用或禁用。这取决于你喜欢什么。

![Enable Tap to click for laptops on Ubuntu 24.04 ](https://itsfoss.com/content/images/2024/05/tap-to-click-ubuntu-24-04.webp)

{% note color:green 💡你也可以使用 「打字时禁用触控板」 功能，它位于触控板设置的顶部。 %}

由于你在笔记本电脑上使用 Ubuntu， 你应该 [使用它的三指滑动手势](https://itsfoss.com/three-finger-swipe-gnome/)。
{% link https://itsfoss.com/three-finger-swipe-gnome/ %}

## 显示电量百分比

无论是智能手机还是笔记本电脑，我都更喜欢关注电池电量。

这样，我就不会收到意外的 “电量不足” 通知。

![Displaying battery percentage on Ubuntu 24.04](https://itsfoss.com/content/images/2024/05/displaying-battery-percentage-ubuntu.png)

您可以从电源设置的底部位置启用此选项。

![img](https://itsfoss.com/content/images/2024/05/display-battery-percentage-ubuntu-24-04.webp)

{% note color:green 💡 您知道您可以检查连接的蓝牙设备的电池电量吗？它显示在电源设置中，但要显示在顶部面板中，您必须使用 [ GNOME 扩展](https://extensions.gnome.org/extension/3991/bluetooth-battery/?ref=itsfoss.com) 。

## 由于不活动而禁用自动锁定

如果你的 Ubuntu 笔记本电脑无人值守，屏幕会自动变暗并锁定系统。 而这只需五分钟即可完成。

目前，这可能是有争议的，因为它肯定是一个「安全功能」，但我不喜欢它。

我不喜欢仅仅 5 分钟没有使用笔记本电脑就再次输入密码。

在**隐私和安全**设置中，有一个专门的屏幕锁定部分。

![Automatic screen lock feature in Ubuntu](https://itsfoss.com/content/images/2024/05/screen-lock-settings-ubuntu-24-04.png)

在这里，你可以很容易地禁用自动屏幕锁定功能。

![Disabling automatic screen lock feature in Ubuntu](https://itsfoss.com/content/images/2024/05/disable-automatic-screenlock-ubuntu.png)

您还可以探索锁屏的其他设置，例如在锁屏上获取通知。

{% note color:green 💡您可以按 Super (Windows) 键 + L 来快速锁定 Ubuntu 系统。 %}

## 使用不同的电源配置

在 Ubuntu 中，你有三种电源模式：

- 性能：高 CPU/GPU 使用率和电池使用时间缩短
- 平衡：标准 CPU/GPU 使用率和电池使用率
- 省电模式：通过降低 CPU/GPU 性能来节省电池电量

不用说，当你没有连接电源时，你最好使用平衡和省电模式。

可以通过单机右上角并单击电源模式选项来访问这些模式。

![Power modes in Ubuntu 24.04](https://itsfoss.com/content/images/2024/05/power-profile-ubuntu-24-04.webp)

您可以在电源设置中探索更多选项。

有些人使用 [tlp](https://linrunner.de/tlp/index.html?ref=itsfoss.com) 来延长 Linux 上的电池寿命。我几年前曾经这样做过，但最近没有这样做，因为至少在默认设置下我没有观察到任何好处。这也与电源配置文件相冲突。

但如果你想了解更多，这里有迈克尔·霍恩的一个很好的视频。

{% video youtube:GDdGK8Z_qzs width:100% autoplay:0 %}

[我的 TUXEDO 笔记本电脑默认预装了 Linux](https://itsfoss.com/get-linux-laptops/)。 由于 [TUXEDO](https://www.tuxedocomputers.com/index.php?ref=itsfoss.com) 是一个 Linux 系统制造商， 他们有自己的 [TUXEDO 控制中心应用程序](https://www.tuxedocomputers.com/en/TUXEDO-Control-Center-TCC.tuxedo?ref=itsfoss.com)可以让你改变到不同的电源配置文件，控制 CPU 风扇，创建自定义配置文件以及进行许多高级更改。请注意，您**不能**在非 TUXEDO 设备上使用它。

{% link https://news.itsfoss.com/tuxedo-infinitybook-pro-16-review/ %}

## 通过分数缩放获得正确显示

我的 TUXEDO InfinityBook 有一个 2K (2560x1600px) 的屏幕. 而我的 Dell XPS 有一个 4K 的屏幕。

图标、字体和其他所有内容在两个屏幕上看起来都很小。 但如果我把分辨率缩放到 200 %，它们看起来就太大了，尤其是在 2K 的屏幕上。

值得庆幸的是，Ubuntu 提供了分数缩放选项。 启用它，你可以将显示缩放 25 %。

![Using Fractional Scaling on Ubuntu 24.04](https://itsfoss.com/content/images/2024/05/enable-fractional-scaling.png)

这样，我在 2K 屏幕上设置了 125 %，在 4K 屏幕上设置了 150 %。

这完全是个人偏好的问题，我很高兴有一个选项来设置这些偏好。

## 你还可以做更多的调整

我将本文限制在以笔记本电脑为中心的调整上。 否则，我通常会在我的Ubuntu 系统上进行更多调整。 夜灯、[点击最小化](https://itsfoss.com/click-to-minimize-ubuntu/) ，和请勿打扰只是我此刻想到的几个功能。

这里还有[一些你可以探索的 Ubuntu 自定义技巧 ](https://itsfoss.com/gnome-tricks-ubuntu/)。

{% link https://itsfoss.com/gnome-tricks-ubuntu/ %}

💬 在笔记本电脑上使用 Ubuntu 或任何其他 Linux 发行版时，您会更改那些设置？ 请在评论中分享。
