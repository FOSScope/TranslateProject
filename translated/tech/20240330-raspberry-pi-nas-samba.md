---
title: '使用 Samba (SMB) 服务器将你的树莓派打造成 NAS'
date: 
author:
- fosscope-translation-team
- cys2004
- <校对者ID>
banner: https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/raspberry-pi-samba-nas.webp
cover: https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/raspberry-pi-samba-nas.webp
categories:
- 翻译
- 技术
tags:
- Samba
- CIFS
- Raspberry Pi
- NAS
authorInfo: |
  via: https://itsfoss.com/raspberry-pi-nas-samba/

  作者：[Abhishek Kumar](https://itsfoss.com/author/abhishek-kumar/)
  选题：[cys2004](https://github.com/cys2004)
  译者：[cys2004](https://github.com/cys2004)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出

---

这是一个适合树莓派初学者的项目，你可以将你的树莓派变成使用 SMB 服务器的 NAS。

<!-- more -->

你是否厌倦了挤满文件的本地存储，以至于寻找文件时就像在进行一场寻宝游戏？

不必担心！今天，我们将把你的树莓派变成一个 **网络附加存储（NAS）** 解决方案。

向本地存储过载的复杂局面说再见吧。想象一下，你的树莓派配备了 **Samba 服务器** ，能够无缝地组织文件，从而实现高效协作、同时访问与可靠备份。

## 什么是 Samba？

Samba 是一个软件套件，它利用 [服务器消息块 （SMB）/ 通用互联网文件系统 （CIFS）](https://learn.microsoft.com/en-us/windows/win32/fileio/microsoft-smb-protocol-and-cifs-protocol-overview?ref=itsfoss.com) 文件共享标准实现了无缝的文件和打印服务互操作性。这一标准被包括 Windows、MacOS、Linux 甚至 Android 在内的多种操作系统广泛支持。

对于树莓派来说，还有其他以 NAS 为导向的解决方案可用，例如 [Open Media Vault](https://www.openmediavault.org/)。我发现设置 SMB 共享是最简单的，如果你对网络存储不太了解，我认为你应该尝试这种无忧的方法。

## 要求

- 树莓派
- SD卡（8 GB 以上）
- 已经安装好的 Raspbian OS（这里提到的命令在该系统上工作）
- 以太网线（可选）
- 键盘和鼠标（可选）
- 外部 HDD/SSD

{% note color:yellow ✋ 树莓派上的 USB 接口可能不足以为外部硬盘供电。因此，我建议你使用外部电源或购买硬盘扩展坞。 %}

## 安装 Samba 及其依赖项

首先，请确保 [在你的树莓派上安装了Raspbian OS](https://itsfoss.com/tutorial-how-to-install-raspberry-pi-os-raspbian-wheezy/)。这里我不会讨论这些步骤。

在 Linux 上工作的第一步是确保你安装了所有最新的软件包。

```bash
sudo apt update && sudo apt upgrade -y
```

要安装 Samba 软件包，你只需要执行`apt-get`命令，因为它们都可以在仓库中找到。

```bash
sudo apt-get install samba samba-common-bin
```

工作到这里还没有完成，因为你还需要创建一个将会被共享的文件夹。这个文件夹甚至可以位于挂载到树莓派的外部驱动器上。

## 创建共享文件夹

在本教程中，我将外部驱动器挂载并在`/media`目录下创建一个新文件夹。

我将给这个文件夹所有的权限，即`读/写/执行（rwx）`，这样我的子网络中有权访问我的服务器的任何人都可以轻松地共享文件。

```bash
sudo mkdir -m 1777 /media/hdd/shared
```

## 编辑 SMB 配置文件

创建好文件夹之后，是时候配置你的 SMB 共享了。你需要做的是编辑`smb.conf`文件，使你的共享在网络上可见。

```bash
sudo nano /etc/samba/smb.conf
```

在这个配置文件中，你需要在底部添加以下代码：

```
[itsfossnas]
path = /media/hdd/shared
writeable=Yes
create mask=0777
directory mask=0777
public=no
```

然后使用`CTRL + X`退出 Nano 编辑器，并按`Y`保存。

在这里，`[itsfossnas]`是我的共享名称，它将用于连接到像`\\localhost\itsfossnas`这样的网络共享地址。

![Editing samba config file](https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/adding-smb-share-in-config-file-samba-tutorial-raspberrypi.webp)

## 为 Samba 共享创建用户

为 Samba 共享创建用户对于访问控制、安全和个性化设置至关重要。

在这个例子中，我将创建一个名为`abhishek`的用户。

```bash
sudo smbpasswd -a abhishek
```

按`Enter`后，它会提示你为这个用户创建一个密码。

![Create Samba user](https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/creating-username-and-password-for-samba-tutorial-raspberrypi.webp)

最后，你需要重启 Samba 服务：

```bash
sudo systemctl restart smbd
```

每次你启动树莓派时，Samba 都会自动重启。

现在是时候连接到你的 Samba 共享了。为此，你需要在网络上定位树莓派。

最简单的方法是在终端上输入`hostname -I`。你也可以检查路由器的 DHCP 记录，它会显示分配给你的树莓派的IP地址。

## 在 Windows 上挂载你的 Samba 服务器

在 Windows 上挂载服务器非常简单。你需要点击位于文件资源管理器顶部的菜单图标`...`，然后屏幕上会弹出一个选项列表，你需要选择`映射网络驱动器`。

我在本教程中使用的是 Windows 11。

![Mount NAS on Windows](https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/file-explorer-mapping-network-drive-samba-tutorial-raspberrypi.webp)

之后，它会要求你为你的共享设置驱动器字母和服务器的地址。在我的案例中，它是`\\192.168.1.11\itsfossnas`。

![Mount NAS on Windows](https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/adding-server-address-with-smb-share-details-samba-tutorial-raspberrypi.webp)

最后，它会提示你输入你的`登录凭据`，即我们在上一步设置的用户名和密码，完成后，只需点击`确定`。

![Mount NAS on Windows](https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/login-your-smb-share-samba-tutorial-raspberrypi-1.webp)

现在，你的驱动器已经成功挂载。

![NAS mounted on Windows](https://static.fosscope.com/articles_img/2024/03/raspberry-pi-nas-samba/mounted-smb-folder-in-windows-explorer-samba-tutorial-raspberrypi.webp)

传输速度将根据你使用的是WiFi还是通过以太网线连接而有所不同。

## 结论

我不会说这会是你的永久存储和备份解决方案，但令人印象深刻的是，这样一个小小的设备能做如此之多的事情。

我认为，在你全力以赴购买一台昂贵的NAS之前，了解一下网络存储方案是非常好的。

希望你学到了一些新东西。欢迎在评论中分享你的经验或是你的 DIY 存储解决方案。
