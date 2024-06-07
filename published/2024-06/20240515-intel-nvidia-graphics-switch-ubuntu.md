---
title: 在 Ubuntu 上切换 Intel 和 Nvidia 显卡
date: 2024-05-18 13:41:37
author:
  - fosscope-translation-team
  - GlassFoxowo
  - void-mori
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/cover.png
cover: https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/cover.png
categories:
  - 翻译
  - 技术
tags:
  - Nvidia
  - Linux
  - Ubuntu
authorInfo: |
  via: https://itsfoss.com/intel-nvidia-graphics-switch-ubuntu/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[GlassFoxowo](https://github.com/GlassFoxowo-Dev)
  校对：[void-mori](https://github.com/void-mori) [Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---


有一个同时配备了 Intel 和 Nvidia 两个显卡的系统？了解如何在两者之间切换。

<!-- more -->

我的 [TUXEDO InfinityBook Pro](https://news.itsfoss.com/tuxedo-infinitybook-pro-16-review/?ref=itsfoss.com) 配备了两个显卡：集成的 Intel 显卡和独立的 Nvidia GeForce 显卡。

如今，笔记本电脑上常见的配置是集成显卡和独立显卡的混合配置。

集成的 Intel 显卡作为主要显卡，处理大多数不太密集的任务而不消耗太多电力，从而延长电池使用时间。

对于游戏、3D 渲染和其他图形密集型工作，应使用独立的 Nvidia GPU。

**在本教程中，我还将向您展示如何在 Ubuntu 及其他 Linux 发行版上在 Intel 和 Nvidia 显卡之间切换。**

有两种方法可以实现这一点。您可以显式地使用 Nvidia 而不是 Intel 来运行应用程序，或者您可以更改设置以始终使用 Nvidia 显卡。如果您使用 Nvidia 专有驱动程序，而不是开源驱动程序，这将更容易。

## 检查您拥有的显卡

{% note color:yellow ✋ 本教程专门针对 Intel 和 Nvidia 显卡（也称为视频卡）设置。它可能不适用于 AMD 显卡。 %}

因此，您必须确保您使用的是 [Nvidia 显卡](https://developer.nvidia.com/?ref=itsfoss.com)。

要在 Linux 中 [检查您的显卡](https://itsfoss.com/check-graphics-card-linux/)，请使用以下命令：

```bash
lspci | grep VGA
```

以下是我的系统显示的内容：

```bash
lspci | grep VGA
00:02.0 VGA compatible controller: Intel Corporation Alder Lake-P GT2 [Iris Xe Graphics] (rev 0c)
01:00.0 VGA compatible controller: NVIDIA Corporation GA104 [Geforce RTX 3070 Ti Laptop GPU] (rev a1)
```

如上输出所示，我的笔记本电脑配有 Intel Iris Xe Graphics 和 Nvidia Geforce RTX 3070 Ti。

确认之后，我们来看如何使用 Nvidia 而不是集成的 Intel 视频驱动程序。

## 方法一：使用 Nvidia 运行某些应用程序

实际上，Ubuntu 提供了一种使用独立 Nvidia 显卡启动应用程序的方法。

在启动器中，当您右键点击图标时，会注意到一个“使用独立显卡启动”的选项。这“[独立显卡](https://www.intel.com/content/www/us/en/support/articles/000057824/graphics.html?ref=itsfoss.com)”就是您的独立显卡，此处为 Nvidia。

![在 Ubuntu 中选择使用独立显卡启动](https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/launch-using-discrete-graphics-card.webp)

在 GNOME 活动区域的应用程序中，您也可以看到此选项。

请注意，并不是每个使用此选项启动的应用程序都会实际使用 Nvidia 显卡。我测试发现，尽管 Firefox 使用独立显卡启动，但许多其他应用程序如视频播放器、Inkscape 等并未如此。

{% note color:cyan 📋 我如何知道某个应用程序是否在使用 Nvidia？我使用了 Nvidia 专有驱动程序附带的 `nvidia-smi` 命令行工具。在本教程的下一部分中，我会讨论这一点。 %}

要从终端使用 Nvidia 驱动程序运行应用程序，您可以使用：

```bash
DRI_PRIME=1 应用名称
```

所以，如果您想用 Nvidia 运行 Firefox，可以这样使用：

```bash
DRI_PRIME=1 firefox
```

此 `DRI_PRIME` 环境变量似乎仅适用于开源的 Nouveau 驱动程序。如果您使用的是专有驱动程序，应使用：

```bash
__GLX_VENDOR_LIBRARY_NAME=nvidia __NV_PRIME_RENDER_OFFLOAD=1 应用名称
```

{% note color:green 💡 使用专有的 NVIDIA 驱动程序可以使切换显卡驱动程序以及监控每个进程的 GPU 使用情况变得更加容易。下一部分将介绍这一点。 %}

## 方法二：使用专有的 Nvidia 驱动程序以及其附加工具

在 GNOME 活动区域中查找“附加驱动程序”工具：

![附加驱动程序工具](https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/ubuntu-additional-drivers-tool.png)

您也可以在“软件和更新”工具中的附加驱动程序工具下找到它。

在这里，确保您使用的是专有的 Nvidia 驱动程序。选择最高版本，除非您拥有一张旧显卡，该显卡由遗留驱动程序（如图中的 470）支持。

![在 Ubuntu 中使用专有的 Nvidia 驱动程序](https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/using-nvidia-properitary-driver-ubuntu.webp)

如果更改显卡驱动程序，**您将需要重启系统。**

在某些情况下，您会被提示签署 MOK。只需使用一个密码，当您重新启动系统并看到蓝色的 MOK 屏幕时，用之前使用的密码进行签署。

无论如何，当您回到系统时，查找名为 NVIDIA X Server 的工具：

![NVIDIA X Server 工具](https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/nvidia-x-server.png)

在这里，从左侧栏中选择 PRIME 配置文件，然后您将看到切换显卡驱动程序的选项。

![NVIDIA 显卡驱动程序选择](https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/make-nvidia-default-graphics-ubuntu.png)

性能模式意味着 Nvidia 将是所有应用程序的主要显卡。

按需模式是默认行为，即始终使用 Intel 集成驱动程序，只有在指定时才使用 Nvidia（如方法一中所见）。

{% note color:green 💡 当您更改显卡配置文件时，您需要注销系统并重新登录以看到效果。 %}

您也可以从命令行将 Nvidia 设置为主要显卡：

```bash
sudo prime-select nvidia
```

```bash
abhishek@itsfoss-tuxedo:~$ sudo prime-select nvidia
[sudo] password for abhishek: 
Info: selecting the nvidia profile
Deleting /lib/modprobe.d/nvidia-runtimepm.conf
Updating the initramfs. Please wait for the operation to complete:
Done
```

或者，如果您想从命令行使用 Nvidia 专有驱动程序运行应用程序，请使用：

```bash
__GLX_VENDOR_LIBRARY_NAME=nvidia __NV_PRIME_RENDER_OFFLOAD=1 application_name
```

## 💡 额外提示：检查每个进程的显卡使用情况

使用 Nvidia 专有驱动程序，您还可以获得另一个方便的 CLI 工具 `nvidia-smi`。

只需运行如下命令：

```bash
nvidia-smi
```

它将一目了然地显示 GPU 使用统计信息：

![nvidia-smi 输出](https://static.fosscope.com/articles_img/2024/05/intel-nvidia-graphics-switch-ubuntu/nvidia-smi.png)

如果您想像 top 命令一样持续监控 GPU 使用情况，可以将其与 watch 命令结合使用，如下所示：

```bash
watch -n1 nvidia-smi
```

它将每秒刷新一次统计信息。使用 Ctrl+C 停止运行程序。

## 结论

我很惊讶地发现，开源的 Nvidia Nouveau 驱动程序没有 CPU 使用情况工具。我认为应该有一个。

专有驱动程序提供了方便的工具来切换显卡驱动程序和监控 GPU 使用情况。

哪个驱动程序表现更好完全取决于您。我将会让您自行实验并得出结论。

🗨️ 在这里提到的步骤仍有问题吗？请在评论中告诉我，我会尽力提供帮助。
