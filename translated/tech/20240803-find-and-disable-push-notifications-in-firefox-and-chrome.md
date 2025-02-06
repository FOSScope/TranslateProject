---
title: 在 Firefox 和 Chrome 浏览器中查找并禁用推送通知
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/disable-push-notifications-chrome-firefox.webp
cover: https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/disable-push-notifications-chrome-firefox.webp
categories:
  - 翻译
  - 技术
tags: 
  - 教程
authorInfo: |
  via: {{via}}

  作者：[Sreenath](https://itsfoss.com/author/sreenath/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

这里介绍如何在 Firefox 和谷歌 Chrome 浏览器中禁用烦人的推送通知。

<!-- more -->

浏览器中的推送通知功能允许网站（在获得许可的情况下）在你的桌面上显示新动态通知。

当你访问一个希望向你发送通知的网站时，会弹出类似这样的窗口：

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/push-notification-displayed-in-firefox-2.webp *Firefox 中的推送通知权限* %}

如果你选择允许，就会开始收到该网站新动态的桌面通知。

例如，如果你是 It's FOSS 社区论坛的成员，当有人回复你的帖子时，你就会收到桌面通知。

许多网站还会在发布新文章时使用推送通知告知你，即使该网站并未在浏览器中打开也会如此。

但在有的时候，这也会很烦人😠 特别是当某个网站开始发送过多或不相关的通知时。

在本文中，我将介绍如何在 Firefox 和 Chrome 这两款互联网上最受欢迎的浏览器中禁用推送通知。

**其他基于 Chromium 内核的浏览器操作过程应该类似**。

## 在 Firefox 中禁用推送通知

下面来看看如何阻止特定网站或多个网站的推送通知。

### 1. 禁用特定网站的推送通知

当你正在浏览某个特定网站时，可以点击地址栏上的网站设置按钮，如下所示：

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/revoke-site-notification-permission-in-Firefox-site-settings-button-1.webp *移除通知权限* %}

这将列出该网站拥有的权限。如果该网站被允许发送通知，点击 **「发送通知」** 旁边的叉号图标来撤销该权限。

### 2. 一次性禁用多个网站的推送通知

**还有另一种方法可以一次性禁用多个网站的通知**。

首先，点击右上角的菜单，然后进入设置。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/select-settings-in-firefox.png *在 Firefox 中选择设置* %}

在设置菜单中，转到 **「隐私与安全」** 标签页，然后向下滚动到 **「权限」** 部分。在这里，点击「通知」项旁边的设置按钮。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/cllick-on-notification-settings-button-firefox.png *在 Firefox 中选择通知设置* %}

在弹出的窗口中，你可以允许或阻止单个网站的通知，也可以撤销所有网站的通知权限（下面会详细介绍）。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/change-individual-site-notification-block-firefox.png *更改单个网站的通知设置* %}

点击 **「保存更改」** 以保存设置。

### 3. 禁用所有网站的推送通知并阻止新请求

在上面看到的权限窗口中，你还可以选择移除所有被允许显示通知的网站。

如果你直接跳到了这一步，别担心，我再告诉你一遍：

转到 **「菜单 → 设置 → 隐私与安全」** 。向下滚动到 **「权限」** 部分，然后选择「通知」旁边的设置按钮。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/cllick-on-notification-settings-button-firefox-1.png *Firefox 中的通知设置* %}

在新窗口中，点击 **「移除所有网站」** 按钮。这将撤销所有的通知权限。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/remove-all-website-notification-permission-and-disable-further.png *移除所有通知权限* %}

{% note color:cyan 💡 如果你愿意，可以选中 **「阻止请求允许通知的新请求」** 复选框。这样做将禁止网站在未来请求通知权限。 %}

完成更改后，点击 **「保存更改」** 按钮完成设置。

## 在 Chrome 中禁用推送通知

适用于谷歌 Chrome 的步骤应该也适用于任何基于 Chromium 内核的浏览器，只是略有不同。例如，微软 Edge 提供了 **「Cookies 和网站权限」** 菜单，而 Brave 提供了 **「网站和防护」** 设置。

它们的工作方式相同，只是找到选项的方式略有不同。

### 1. 禁用单个网站的推送通知

如果你想移除当前正在访问的网站的通知权限，点击地址栏上的 **「权限」** 按钮。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/click-on-site-settings-button-in-the-address-bar-to-get-settings.png *点击地址栏上的网站设置按钮* %}

在下拉菜单中，禁用发送通知的权限。可以关闭「通知」选项，也可以点击「通知」下方的「重置权限」按钮。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/reset-the-notification-permission-of-a-site-in-chrome-browser.png *重置网站通知权限* %}

### 2. 禁用多个网站的通知

在 Chrome 中，你可以指定一个包含网站地址的阻止列表。这样，你将不会收到这些网站的通知。

为此，和上一步一样，转到 **「设置 → 隐私与安全 → 网站设置 → 通知」**。

现在，向下滚动到 **「自定义行为」** 部分。在这里，你可以使用 **「添加」** 按钮添加你希望默认阻止其通知的网站的完整地址。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/block-selected-sites-to-not-send-notiification.png *阻止选定网站发送通知* %}

从上面的截图中可以看到，我已经阻止了几个网站发送通知。

### 3. 在 Chrome 中完全禁用通知

不想让任何网站发送通知？你也可以做到这一点。

首先，转到 **「设置 → 隐私与安全 → 网站设置 → 通知」**。

在 **「默认行为」** 下，选择 *「不允许网站发送通知」* 按钮。

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/remove-site-notifications-alltogether-in-chrome.png *不允许网站发送通知* %}

就是这样！现在你将不会收到任何网站的通知。

💬 *你对浏览器中的推送通知有什么默认偏好？你觉得它们有用吗，还是一直将其禁用？欢迎分享你的想法！*