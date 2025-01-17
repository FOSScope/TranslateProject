---
title: 修复 Ubuntu 启动器中应用程序图标缺失问题
date: 2024-09-15 12:58:12
abbrlink: 20240621-fixing-applications-icon-missing-from-the-launcher-in-ubuntu
author:
  - fosscope-translation-team
  - excniesnied
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/fix-missing-app-icon-ubuntu.webp
cover: https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/fix-missing-app-icon-ubuntu.webp
categories:
  - 翻译
  - 技术
tags:
  - Ubuntu
  - 故障排除
authorInfo: |
  via: https://itsfoss.com/ubuntu-app-icon-missing

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesnied](https://github.com/excniesNIED)
  译者：[excniesnied](https://github.com/excniesNIED)
  校对：[Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

某些应用程序在 Ubuntu 的启动器中不显示图标？ 解决方法如下。

<!-- more -->

最近，我在 Ubuntu 24.04 中遇到了一个奇怪的问题。

当我运行一些应用程序时，在启动器中显示的不是它们的图标，而是一个齿轮/设置符号。

{% image https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/missing-icons-from-launcher-ubuntu.webp *某些应用程序图标在启动器中不显示* %}

这一点特别奇怪，因为这些应用程序确实有图标，而且缩略图在活动区中显示正常。

{% image https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/applications-icons-displayed-in-gnome-activity-menu.webp *但应用程序图标在 GNOME 活动中显示正常* %}

更令人惊讶的是，Ubuntu 预装的 Transmission torrent 客户端也出现了这种情况。

在本教程中，我将分享如何修复图标丢失问题。但在此之前，先让我讨论一下这里出了什么问题。

{% note color:red 🚧 本教程仅适用于 GNOME 桌面环境。 %}

## 元素失踪之谜

好吧，事情是这样的。您安装的每个应用程序都应该有一个 `.desktop` 文件，其中包含各种信息，包括应用程序图标的位置。

这个 `.desktop` 文件对于桌面整合至关重要。没有它，就无法在菜单中搜索已安装的应用程序，也不会显示缩略图和图标。

但在我这个情况下，ONLYOFFICE 和 Transmission 的桌面文件都在 `/usr/share/applications` 目录中。 我甚至还确认了图标图像文件是存在的。

这让我百思不得其解，于是我开始查阅 GitHub 和论坛上的讨论。就在这时，我发现了关于 [某些 KDE 应用程序中缺少 `WM_CLASS` 属性](https://askubuntu.com/questions/1251172/active-application-icon-not-shown-on-dock) 导致类似问题的讨论。

我使用的并非 KDE，但这是一个正确的方向。[这篇博客文章](https://ubuntuhandbook.org/index.php/2024/04/missing-icon-dock-ubuntu-2404/) 证实了我的观点。

{% note color:cyan **📋简而言之** 您需要获取 `WM_CLASS` 属性，并用这个值更新应用程序的 `.desktop` 文件。 %}

## 修复启动器中应用程序图标缺失问题

{% note color:yellow ✋ 尽管我试图详细讲解每一步，但您仍需付出一些努力。这不是那种只需运行一个命令就能解决问题的方案。您需要将我的示例作为参考，并将其应用到您的具体情况中。您需要具备 Linux 命令行的基本知识。 %}

### 第 0 步：运行相关应用程序

您必须运行图标丢失的应用程序。这一点至关重要。

### 第 1 步：获取应用程序的 `WM_CLASS` 属性

如果您使用的是 Xorg 而不是 Wayland，这一切都会变得简单一些。在终端中运行 `xprop WM_CLASS` 命令，光标会变成十字光标，点击所需应用程序即可获取其 `WM_CLASS` 属性。

但这在 Wayland 上是不可能的，所以我们还需要进一步操作。

按 {% kbd Alt %} + {% kbd F2 %} 键启动「运行命令」对话框。您的键盘上应该有一个 {% kbd F2 %} 功能键。找找看。有时，它们需要以 {% kbd Fn %} + {% kbd 2 %} 的方式运行。我会让您自行解决这个问题。

按 {% kbd Alt %} + {% kbd F2 %} 键会弹出一个对话框。 在此输入 `lg`（小写 LG）：

![Entering debug mode in GNOME](https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/bring-debug-mode-gnome.webp)

这将调出 GNOME 的集成调试器和检查器工具。在此阶段，鼠标和键盘的功能有限。在这里，点击「窗口」选项，它将显示每个运行中应用程序窗口的 `WM_CLASS` 属性。

{% image https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/get-wm-class-property-gnome.webp *如果无法正常显示，点击以展开* %}

请注意，在这个阶段复制粘贴在此示例中无法使用。我将其截图下来作为（后续操作的）参考。

按 {% kbd Esc %} 键关闭调试器。

### 第 2 步：编辑 `.desktop` 文件

{% note color:cyan 📋 如果您没有太多编辑此类配置文件的经验，请在修改之前备份一份 `.desktop` 文件。 %}

下一步是编辑应用程序的 `.desktop` 文件。您应该在 `/usr/share/applications` 目录中找到它。如果没有，也可以尝试在 `~/.local/share/applications` 和 `/var/lib/flatpak/exports/share/applications/` 目录中查找。

现在，您可以使用 Nano 在终端中编辑文件。示例如下：

```Bash
sudo nano /usr/share/applications/onlyoffice-desktopeditors.desktop
```

**但如果您不习惯这样做，也可以用图形化程序来实现。** 只需转到应用程序 `.desktop` 文件的位置即可。

在文件管理器中，您可以点击「其他位置」，然后点击「Ubuntu」来访问根目录。

![Accessing root directory in Ubuntu](https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/access-root-directory-ubuntu.webp)

从那里，您可以进入 `user->share->applications` 文件夹。您也可以直接在文件管理器的地址栏中输入 `/usr/share/applications` 以快速跳转到该位置。

**在文件中， `[Desktop Entry]` 部分下**，添加一行内容

```
StartupWMClass=[上一步您得到的 WM_Class 值]
```

![Editing desktop file](https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/editing-deskto-file.webp)

保存文件。您必须输入账户密码才能保存文件。

效果立竿见影，无需重启，甚至无需注销。保存文件后，图标几乎会立即显示在启动器中。

![Missing application icon fixed in Ubuntu](https://static.fosscope.com/articles_img/2024/08/fixing-applications-icon-missing-from-the-launcher-in-ubuntu/missing-application-icon-fixed-ubuntu.webp)

我发现获取应用程序的 `WM_CLASS` 属性时鼠标和键盘可进行的操作有限。`WM_CLASS` 文本无法复制。因此，我保留界面的截图，在截图中查看 `WM_CLASS` 值，并手动输入。

## 结论

修复缺失的图标是件好事。虽然费了点力气，但在这个过程中我学到了一些新东西。这就是我喜欢故障排除的原因 —— 您学到您永远不会知道的东西。

我不知道该怪 Ubuntu 还是怪 GNOME。但这种用户体验很差，尤其是在使用默认安装的应用程序时。

*🗨️ 希望教程不会过于复杂。 它能帮您解决 Ubuntu 图标丢失的问题吗？*
