---
title: 如何在树莓派上设置静态 IP 地址
date: 2024-08-12 11:45:14
abbrlink: 20240406-set-static-ip-raspberry-pi
author:
  - fosscope-translation-team
  - GlassFoxowo
  - excniesnied
banner: https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/set-static-ip-raspberry-pi.png
cover: https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/set-static-ip-raspberry-pi.png
categories:
  - 翻译
  - 技术
tags:
  - 树莓派
  - 网络
authorInfo: |
  via: https://itsfoss.com/raspberry-pi-static-ip/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[GlassFoxowo](https://github.com/GlassFoxowo-Dev)
  译者：[GlassFoxowo](https://github.com/GlassFoxowo-Dev)
  校对：[excniesNIED](https://github.com/excniesNIED)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

了解为树莓派设置静态 IP 的正确步骤，这样就能始终使用相同的 IP 进行访问。

<!-- more -->

最近，我在我的树莓派上设置了 Jellyfin 媒体服务器。我的树莓派通过无线连接到路由器，在这个设置中遇到的一个问题是在电视或其他设备上访问媒体服务器。

为什么呢？因为树莓派有时会在重新启动之间被分配一个随机的 IP 地址。而且由于我试图通过 IP 地址访问运行在树莓派上的媒体服务器，这就成了一个问题。

每次 IP 地址更改时，我都不得不手动在电视上输入 IP 地址。找到树莓派的 IP 地址是另一个挑战。

这就是静态 IP 的作用所在。如果您的树莓派使用静态 IP，IP 地址在重新启动之间保持不变。

在许多情况下，最好为树莓派分配一个静态 IP。在本教程中，我将讨论如何实现这一点。

## 在树莓派设备上设置静态 IP 与在路由器上设置静态 IP

是的！有两种方法让您的树莓派拥有静态 IP。

- 您可以在树莓派上设置静态 IP
- 您可以让您的路由器为树莓派分配一个静态 IP

这两种方法都有其利弊。

**假设您在树莓派上设置了静态 IP**。您的树莓派将始终从路由器获取相同的 IP 地址（假设为 192.168.1.51）。只要路由器保持不变，这就没问题。如果您更换路由器，并且新路由器坚持使用不同的子网（假设在 172.16.12.0/36 范围内），那么您的树莓派将无法像以前那样连接到 WiFi。您将不得不再次手动更新树莓派上的网络设置以使用新的 IP 范围。当您只有几个树莓派设备，并且可以直接登录到它们（而不是 SSH）或通过以太网电缆连接到它们时，这可能起作用。对放置在家中任意位置的一组树莓派机群而言亦是如此。

**假设您想要从路由器为树莓派分配静态 IP**。这样，您不会在树莓派上更改任何内容。如果更改了路由器，树莓派将通过 DHCP 服务器自动分配 IP 地址。问题在于，在所有路由器上为设备分配静态 IP 并不容易。一些互联网公司提供的路由器几乎没有配置更改的余地。

{% note color:green 📑 总之，如果您将来可以轻松访问设备物理上，您应该在树莓派上设置静态 IP。 %}

我无法展示如何在路由器上为不同设备分配静态 IP，因为这取决于您拥有的路由器类型。因此，我将讨论如何在树莓派本身上设置静态 IP。

## 在树莓派上设置静态 IP

该过程包括以下四个步骤：

- 获取树莓派的当前 IP 地址（如果您想将其用作静态 IP）
- 获取网关 IP（路由器的 IP）
- 获取 DNS 服务器地址（可选）
- 使用上述信息更改网络配置

前三步在命令行中可以很容易地完成。第三步可以在命令行和 GUI 中都很容易地完成。

{% note color:cyan 📑 确保您的树莓派已连接到路由器。如果通过 SSH 连接到树莓派，您也可以按照这些步骤操作。 %}

### 第1步：获取树莓派的 IP 地址

如果您想使用当前 IP 地址作为静态 IP，

这很简单。在终端中，键入以下命令：

```bash
hostname -I
```

您还可以使用此命令：

```bash
ip a
```

两者都会给您当前树莓派的 IP 地址。

![获取树莓派的 IP 地址](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/get-ip-address-raspberry-pi-os.webp)

如上面的截图所示，我的树莓派的 IP 地址是 192.168.1.34。

### 第2步：获取网关 IP

这也相当简单。要获取网关 IP 地址（您的路由器的 IP 地址），请使用此命令：

```bash
ip route | grep default
```

如下面的截图所示，在我的情况下，网关 IP 是 192.168.1.1。

![获取网关 IP 地址](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/gateway-ip-raspberry-pi.png)

### 第3步：获取 DNS 服务器详细信息（可选）

有些人喜欢保持当前系统上使用的相同 DNS 服务器。我认为您也可以不这样做。大多数家庭用户都会自动处理 DHCP 服务器。

但是，如果您愿意，您可以使用以下命令获取 DNS 服务器地址：

```bash
grep nameserver /etc/resolv.conf
```

![DNS服务器 IP 地址](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/dns-server-ip-raspberry-pi.png)

{% note color:cyan 📋 到目前为止，您必须意识到您为特定的网络连接设置了静态 IP。如果将树莓派连接到其他网络，它将不会使用相同的静态 IP 地址。 %}

### 第4步（终端方法）：更改网络配置以设置静态 IP

如果您通过 SSH 访问树莓派，或者如果您更喜欢使用命令行，您可以使用 nmtui（终端中的网络管理器）工具。

{% note color:yellow ✋ 这些步骤已在树莓派 5 上进行过测试。如果您的系统没有安装 `nmtui` 包，您可以安装它并继续遵循说明进行操作。 %}

运行此命令：

```bash
sudo nmtui
```

您将看到一个类似于此的界面。在这里，选择**编辑连接**并按 Enter。

![在网络管理器中编辑网络连接](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/network-manager-terminal.png)

{% note color:green 💡 在 TUI（终端用户界面）工具中，使用上下箭头键在选项之间移动。您可能还需要使用 tab 键切换到其他选项。 在选定的选项上按回车键。 %}

它将显示您在树莓派上过去的连接情况。我相信您想为当前连接的网络设置静态 IP。向下移动到适当的网络。现在按 tab 键几次以选择编辑选项，然后按 Enter 键。

![在 nmtui 中编辑网络连接](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/edit-network-connection-nmtui.png)

使用箭头键再次向下滚动到 **IPv4 配置**选项。将其从**自动**更改为**手动**。

![更改IPv4配置](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/change-ipv4-configuration-raspberry-pi.png)

接下来，选择 **IPv4 配置**一行的 **显示** 选项。

![通过更改 IPv4 配置在树莓派上设置静态 IP](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/change-ipv4-configuration-raspberry-pi-1.png)

再次使用箭头键向下移动并到达 IPv4 配置部分。这次，您将看到添加地址、网关和 DNS 服务器的选项。

![IPv4 配置更改](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/editing-ipv4-config-nmtui-raspberry-pi.png)

转到地址行并点击 Enter 键。它可能会带您回到开头。再次向下滚动。

{% note color:red ✋ 请务必以 IP 地址/24 的格式输入您选择的 IP 地址和子网掩码。 %}

![在树莓派上设置静态 IP](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/changed-ipv4-config-raspberry-pi.png)

填写所有详细信息，例如 IP 地址与掩码、网关 IP 和 DNS。

![更改 IPv4 配置以在树莓派上设置静态 IP](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/all-ipv4-settings-changed-raspberry-pi.png)

请注意，我在 DNS 中也使用了网关 IP。 我还添加了 [Cloudflare 的 DNS](https://www.cloudflare.com/en-gb/learning/dns/what-is-1.1.1.1/?ref=fosscope.com) 1.1.1.1 作为替代。

**填写所有详细信息后，向下滚动到底部，选择确定并按 Enter 键。**

您的更改将被保存。您可以以同样的方式退出 nmtui 界面（按**返回**，然后选择**退出**选项）。

重新启动您的树莓派以使更改生效。您已成功在树莓派上设置了静态 IP。

### 第4步（GUI 方法）：更改网络配置以设置静态 IP

您还可以从树莓派 OS 的图形界面实现相同的效果。

首先，单击网络图标，然后转到高级选项，点击编辑连接。

{% image https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/edit-connections-to-set-static-ip.webp 在树莓派中编辑连接 %}

在这里，您转到 IPv4 设置，将其设置为手动，然后添加所有详细信息，例如 IP 地址、掩码、网关 IP、DNS 服务器等。您就掌握了所有细节。

![在树莓派上设置静态 IP](https://static.fosscope.com/articles_img/2024/04/set-static-ip-raspberry-pi/editing-network-connections-to-set-static-ip.webp)

重新启动您的系统，您会看到静态 IP 现在已在您的树莓派上设置。

## 返回非静态 IP

如果您不想在树莓派上再使用静态 IP，您可以很容易地恢复到动态 IP。

如何做？只需再次编辑相关的网络连接。这次，将 IPv4 配置更改为“自动”，并保存您的更改。就是这样。您不必再提供 IP 地址、网关 IP 等。

## 结论

正如我在本教程开始时提到的，您应该从路由器端使用静态 IP，特别是如果您的树莓派不容易被物理访问。

但是，如果您的设备一直在您手中，您有权访问和更改其配置。

希望本教程对您在 Raspberry Pi 上设置静态 IP 有所帮助。 如有任何问题，请告诉我。
