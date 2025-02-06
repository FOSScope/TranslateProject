---
title: 我是如何安装 Armbian 桌面系统的
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/install-armbian-sbc.png
cover: https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/install-armbian-sbc.png
categories:
  - 翻译
  - 技术
tags: 
  - Armbian
authorInfo: |
  via: https://itsfoss.com/install-armbian/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesnied](https://github.com/excniesnied)
  译者：[excniesnied](https://github.com/excniesnied)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

以下是我在瑞芯微单板计算机（SBC）上安装 Armbian 桌面系统的过程。

<!-- more -->

Armbian 是一个很棒的项目。虽然 [树莓派有众多操作系统](https://itsfoss.com/raspberry-pi-os/)，但 Armbian 是适用于 [众多类似树莓派的单板计算机](https://itsfoss.com/raspberry-pi-alternatives/)（SBC）设备的操作系统。

如果你使用的不是树莓派设备，那你一定要试试看。

最近，我在我的 [ArmSoM Sige7 开发板](https://www.armsom.org/sige7) 上安装了 Armbian，我想分享一下我所遵循的安装过程。

安装步骤相当简单：
- 为你的单板计算机下载合适的 Armbian 镜像
- 将 Armbian 镜像写入 micro SD 卡
- 从 micro SD 卡启动设备并进行初始设置

让我们详细了解一下。

{% note color:cyan 📋 正如标题所示，本文针对的是 Armbian 桌面系统，因此这里的安装过程并非无界面安装。 %}

## 选择正确的镜像（这很重要）

尽管从名称上看，Armbian 是适用于 ARM 设备的 Debian 系统，但实际上它的功能远不止于此。

**Armbian 同时提供 Ubuntu 和 Debian 版本的构建**。有多种适用于服务器（无桌面环境）和桌面（带有 GNOME 或 Xfce）的版本可供选择。还有一些特殊版本可用于搭建 Home Assistant 和 Open Hab。

现在，选择哪个版本完全取决于你自己。如果你更熟悉 Debian，那就选择 Debian 版本；否则，选择 Ubuntu 版本。

如果你对这两个系统都不太熟悉，那么可以选择 Ubuntu，因为它似乎更受欢迎，尤其在初学者中。

这还没完。Armbian 有三类镜像：
- 白金支持的单板计算机
- 标准支持的单板计算机
- 社区支持的单板计算机
- 通用镜像

![Armbian 白金支持的开发板](https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/armbian-platinum-support-download.webp)

市面上有众多的单板计算机，Armbian 旨在为大多数（如果不是全部）单板计算机提供支持。这就是为什么他们为不同的单板计算机提供不同的镜像。你应该查找你的单板计算机，看看 Armbian 是否为你的开发板提供了专用镜像。

一些单板计算机供应商，如香蕉派（Banana Pi）等，与 Armbian 建立了合作关系，因此它们属于「白金」支持类别。这些开发板有望获得更好的硬件支持。

<center>{% button "下载 Armbian" https://www.armbian.com/download/ %}</center>

如果你在白金、标准或社区支持类别中找不到你的开发板，可以从主页下载通用的 Armbian 镜像。它可能能完全正常工作，也可能不能。

{% note color:cyan 📋 我使用的是 ArmSoM Sige7 设备，它和香蕉派 M7 是一样的。但我在这里使用的是 ArmSoM 提供的自定义 Armbian 版本。其他 Armbian 桌面版本的安装过程应该是相同的。 %}

## 准备 micro SD 卡

我使用 [Linux 版的 Etcher](https://itsfoss.com/install-etcher-linux/) 来制作 Armbian 的 micro SD 卡。Etcher 是一款跨平台工具，你也可以在 Windows 和其他平台上轻松使用它。

<center>{% button "下载 Etcher" https://etcher.balena.io/ %}</center>

它为 Linux 提供了 AppImage 格式。如果你不熟悉 AppImage，请阅读我们的 [使用 AppImage 的指南](https://itsfoss.com/use-appimage-linux/)。

使用 Etcher 很简单。将你的 micro SD 卡插入计算机，然后运行 Etcher。它会立即识别出 SD 卡。浏览下载好的 Armbian.img 文件，然后点击「写入」。

![img](https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/burn-armbian-to-sd-card.png)

等待几分钟，让写入过程完成。如果你的 SD 卡速度较慢，可能需要一些时间。

![将 Armbian 镜像写入 micro SD 卡](https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/burning-armbian-to-sd-card.png)

写入过程完成后，取出 micro SD 卡，准备好你的单板计算机。

{% note color:cyan 📋 如果你在 Ubuntu 系统中尝试弹出新创建的名为 `armbi_root` 的 Armbian SD 卡，可能会出现类似「D - Bus 接口无对象」的错误。这没关系，直接取出 micro SD 卡即可。 %}

## 在 ARM 开发板上安装 Armbian

{% note color:yellow ✋ 使用最新镜像时，可能会遇到启动和其他问题。在这种情况下，你应该从存档中为你的设备下载稍旧一些的镜像，看看是否能解决问题。如果你能在官方论坛上向开发人员反馈这个问题，那就更好了。 %}

将 micro SD 卡插入你的 ARM 开发板。将开发板连接到显示器、键盘、鼠标和电源。如果能连接到以太网端口会更好，但这不是必需的。

设备通电后，几秒钟内你应该会看到 Armbian 的标志。之后，你会看到一个黑色屏幕，并有设置 root 密码的选项。

![首次启动 Armbian 时设置 root 密码](https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/armbian-set-root-password.webp)

{% note color:green 💡 如果你遇到要求登录并输入密码的界面，请记住默认用户是 root，默认密码是 1234。输入后，你将被要求创建 root 密码。 %}

创建好 root 密码后，你将被要求在 bash 和 zsh 之间选择默认 shell。如果你不知道 zsh 是什么，那就选择 bash。

之后，你将被要求创建一个新用户并设置其密码。这个用户将具有 sudo 权限，你可以使用它以 sudo 身份运行命令。

![在 Armbian 中设置用户](https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/armbian-create-user-setup-shell.webp)

由于我连接了以太网，所以系统知道我的地理位置，并根据此建议相应的语言环境。如果你还没有连接到互联网，则需要手动提供合适的选项。

![在 Armbian 中设置语言环境](https://static.fosscope.com/articles_img/2024/08/how-i-installed-armbian-desktop/armbian-set-locale.webp)

设置好语言环境后，系统应该会启动到桌面环境。

{% note color:yellow ✋ 当我将新创建的 Armbian SD 卡连接到 4K 显示器时，没有显示初始设置界面。将其连接到普通的全高清显示器则可以正常显示。不过，初始设置完成后，4K 显示器就可以正常使用了。 %}

## 享受 Armbian

Armbian 使用的是大家熟悉的 APT 包管理器，如果你曾经使用过基于 Debian/Ubuntu 的发行版，应该不会感到陌生。

我分享了我在 [基于瑞芯微的 ArmSom Sige7 单板计算机](https://itsfoss.com/arosom-sige7-review/) 上的安装过程。我希望其他单板计算机的安装过程也是一样的。如果你遇到任何问题，请告诉我。 