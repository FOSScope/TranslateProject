---
title: 如何在 VirtualBox 上备份或克隆虚拟机
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - deepseek-r1
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/backup-virtualbox.webp
cover: https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/backup-virtualbox.webp
categories:
  - 翻译
  - 技术
tags: 
  - VirtualBox
authorInfo: |
  via: {{via}}

  作者：[Ankush Das](https://itsfoss.com/author/ankush/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：DeepSeek R1
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

无论你是想要复制虚拟机，还是希望安全地存储备份，VirtualBox 都能让你轻松实现。

<!-- more -->

使用虚拟机可以在许多方面简化操作，尤其是当你使用 Linux 时。无论你是想测试某个发行版、进行安全研究，还是其他任何操作，虚拟机总能派上用场。

如果你对此感兴趣，可以阅读我们关于 [在虚拟机中运行 Linux 的原因](https://itsfoss.com/why-linux-virtual-machine/) 的文章。

假设你已经设置好了虚拟机，并且知道如何根据你的使用场景 [配置虚拟机](https://itsfoss.com/virtualbox-change-vm-config/)，那么接下来你需要掌握的关键技能就是**备份或克隆虚拟机**。

通过备份和克隆，你可以：

- 在错误修改后快速恢复配置和文件
- 轻松将虚拟机迁移到另一台系统
- 无需再次经历设置过程，快速创建虚拟机的另一个实例

## 在 VirtualBox 上备份虚拟机

你可以通过三种方法在 VirtualBox 上备份虚拟机：

- **完整备份虚拟机文件**（复制粘贴）
- **导出虚拟机**：以便在云端部署或迁移到其他虚拟化程序。
- **创建快照**：如果你不想备份整个虚拟机，而只想备份当前状态。

### 1. 通过复制粘贴虚拟机文件夹进行备份

在 VirtualBox 上备份虚拟机非常简单，但如果你使用的是其他 [虚拟化软件](https://itsfoss.com/virtualization-software-linux/)，过程可能会有所不同。

假设你已经设置并列出虚拟机，以下是你可以做的：

1. 首先，如果虚拟机正在运行，你需要将其关闭。
2. 进入 VirtualBox，右键点击你想要备份的虚拟机，找到「**在资源管理器中显示**」（Windows）或「**在文件管理器中显示**」（Linux）的选项。

![img](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/virtualbox-file-manager.png)

这将显示虚拟机的文件内容：

![fedora vm 文件内容](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/fedora-vm-files.png)

1. 接下来，你需要导航到其父文件夹 **VirtualBox VMs**，然后找到你想要备份的文件夹：

![fedora vm 文件夹](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/fedora-vm-folder.png)

1. 现在，将虚拟机的文件夹复制到你希望存储备份的位置（云端/异地或本地）。

{% note color:green 💡 对于高级使用场景，如果你不想关闭虚拟机，你需要使用第三方备份工具，如 [Timeshift](https://itsfoss.com/backup-restore-linux-timeshift/)（根据你的客户操作系统），从虚拟机内部启动备份。 %}

如果你希望在恢复时检查备份的完整性，可以决定在备份期间为虚拟机文件夹 [创建哈希值](https://itsfoss.com/checksum-tools-guide-linux/)。

### 2. 导出虚拟机

![导出虚拟机](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/export-option-virtualbox.png)

除非你希望在云端部署虚拟机、迁移到其他虚拟化程序（如 VMware），或将其用作预配置的虚拟机模板，否则你不需要导出虚拟机。

因此，对于大多数人来说，这可能是一个多余的选项，因为备份和克隆（下面会讨论）应该足够了。

通常，你会以 OVF（开放虚拟化格式）包的形式导出，文件扩展名为 .OVA。这是一种跨平台的文件格式，可以帮助你将虚拟机迁移到其他程序和机器上。

![ovf 导出](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/virtualbox-export-settings.png)

你可以选择仅导出**清单文件**（仅导出虚拟机的设置），或者连同**镜像一起导出**，以便迁移客户操作系统。

不幸的是，我无法在 VMware 上成功使用它，但在另一台电脑上的 VirtualBox 上尝试时，它运行良好。

当你继续操作时，可以根据需要自定义/标记字段。

![virtualbox 导出](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/virtualbox-export.png)

至于 **OCI**（Oracle 云基础设施）格式，它是为需要远程云服务器的高级用户准备的。此外，导出为这种格式需要满足一系列要求。如果你需要，可以遵循 [官方文档](https://docs.oracle.com/en/virtualization/virtualbox/6.0/user/ovf.html)。

### 3. 创建快照

![virtualbox 快照选项](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/virtualbox-snapshots-1.png)

当你点击菜单图标（带有三条线）时，可以访问快照选项，如上图所示。

当你为虚拟机创建快照时，你并不是在备份整个虚拟机，而是备份其当前状态，包括虚拟机配置、文件状态和设置。

你可以将其视为增量备份（尽管技术上并不完全相同）。

![创建 virtualbox 快照](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/snapshot-take.png)

因此，如果你希望在虚拟机中有一个恢复点，你可以选择创建快照。如果你删除了一个文件，它将在较早的快照中恢复。因此，如果你恢复到某个快照，当前所做的所有更改都将消失。

你可以创建任意数量的快照，这些快照不会像完整备份那样占用大量空间。

## 恢复虚拟机

根据你拥有的备份类型，你可以通过三种不同的方式恢复虚拟机：

- 恢复文件夹
- 导入虚拟机（从 .ova 文件）
- 恢复快照

### 1. 恢复文件夹

你需要将虚拟机文件夹放置到 VirtualBox 的默认存储路径中（无论你自定义了什么路径）。只需将文件夹复制粘贴回虚拟机存储路径即可。

默认路径如下：

- **C:\Users\Ankush Das\VirtualBox VMs** → Windows
- **/home/itsfoss/VirtualBox VMs** → Linux (Ubuntu)

**推荐阅读 📖**

{% link https://itsfoss.com/windows-enable-virtualization/ 如何在 Windows 上启用虚拟化 icon:https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/preparing-windows-system-for-vms.png %}

### 2. 导入虚拟机

根据导出的类型，你可以导入虚拟机设置，或者连同镜像一起导入虚拟机。

![virtualbox 导入设备选项](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/virtualbox-import-menu.png)

前往菜单栏，**文件 → 导入设备**，然后选择导出的文件。

你可以尝试将其导入到其他虚拟化程序，但为此，你需要查看你想要导入的程序的文档，了解如何成功导入。

![导入快照 virtualbox](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/import-virtualmachine-option.png)

如果你将其导入到 VirtualBox，它应该可以顺利运行。

### 3. 恢复快照

![恢复快照 virtualbox](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/snapshot-restore.png)

你需要前往创建虚拟机快照的相同位置。只需选择你想要恢复的快照，然后点击它即可恢复，如上图所示。

## 在 VirtualBox 上克隆虚拟机

如果你想在不影响原始设置的情况下创建虚拟机的精确副本，最好克隆你的虚拟机。

当然，你需要确保你的系统有足够的空闲空间来容纳它。你可以在操作之前[释放空间](https://itsfoss.com/free-up-space-ubuntu-linux/)。

克隆选项可以在你**右键点击 VirtualBox 程序中列出的虚拟机**时的上下文菜单中找到。以下是它的样子：

![virtualbox 中的克隆选项](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/clone-vm-virtualbox-option.png)

接下来，你将看到一个屏幕，可以自定义克隆的名称、选择存储路径（相同或不同）、MAC 地址策略、使用相同的磁盘名称等。

![fedora 克隆选项](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/clone-options.png)

一旦你继续操作（或点击专家模式），你将获得选择「**完整克隆**」或「**链接克隆**」的选项。如下图所示，链接克隆将不是一个独立的实例，而是会创建当前虚拟机的快照。因此，你需要决定这是否是你想要的。

![fedora 克隆类型](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/clone-types.png)

{% note color:green 💡 你总是可以轻松移动完整克隆。但在另一种情况下，你需要迁移整个原始虚拟机和链接克隆。 %}

在这个例子中，我选择了「**完整克隆**」，然后点击「**完成**」以完成克隆过程。你将在 VirtualBox 程序中看到另一个虚拟机被列出。

就是这样！你可以在这里看到它：

![fedora 克隆在 virtualbox 中](https://static.fosscope.com/articles_img/2024/08/how-to-back-up-or-clone-a-virtual-machine-on-virtualbox/fedora-clone-virtualbox.png)

💬*你最喜欢列表中的哪个选项？或者有其他有趣的终端技巧吗？请在下面的评论中分享你的想法。*