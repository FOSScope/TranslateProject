---
title: 谷歌浏览器将逐步禁用 uBlock Origin 等扩展程序：以下是您能做的事情！
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/google-phase-out-manifest-3.webp
cover: https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/google-phase-out-manifest-3.webp
categories:
  - 翻译
  - 新闻
tags: 
  - Google Chrome
authorInfo: |
  via: https://news.itsfoss.com/google-chrome-disable-extensions

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true
translated: true
proofread: false
published: false
---

谷歌浏览器正在通过逐步淘汰旧版扩展程序，为迁移至 Manifest v3 做准备。

<!-- more -->

无论您喜欢与否，[谷歌浏览器（Google Chrome）](https://www.google.com/chrome/)在桌面端和移动端都是全球使用最广泛的网络浏览器。对于桌面用户而言，它有一个显著的优势，那就是可以使用扩展程序来进一步增强浏览器的功能。

如果您最近一直在关注新闻，那您一定听说过，谷歌正在逐步淘汰 Manifest V2 扩展程序，为 Manifest V3 扩展程序铺平道路。据说这一举措旨在提升隐私性、安全性和性能。

至于 Manifest，它是一个 [JSON 文件](https://developer.chrome.com/docs/extensions/reference/manifest)，伴随着扩展程序一起，由浏览器读取以获取重要信息，如扩展程序的名称、版本号、所需权限等。

根据他们的 Manifest V2 [淘汰计划](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline)，开发者在今年 [早些时候](https://blog.chromium.org/2024/05/manifest-v2-phase-out-begins.html) 表示，谷歌浏览器将于 2024 年 6 月开始淘汰进程，首先从谷歌浏览器的 *Beta*、*Dev* 和 *Canary* 渠道开始。

他们已经在 [Chrome 网上应用店](https://chromewebstore.google.com/) 上移除了 Manifest V2 应用的“*精选*”徽章，这也影响了包括 uBlock Origin 在内的一些受欢迎的扩展程序。

而且，他们并不打算止步于此。[uBlock Origin](https://github.com/gorhill/uBlock) 可能需要继续关注相关进展。

## uBlock Origin 即将在谷歌浏览器上消失？😨

![a screenshot of the ublock origin extension listing on the chrome web store with a warning](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_a.webp)

是，也不是。您看，谷歌浏览器现在已经开始在 Chrome 应用商店 [页面](https://chromewebstore.google.com/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm) 上显示 uBlock Origin 的警告信息：

> 此扩展程序未遵循 Chrome 扩展程序的最佳实践，因此可能很快将不再受支持。

此外，在搜索 uBlock Origin，搜索栏中没有将其显示在搜索结果的顶部，但在搜索结果页面上却将其置顶显示。

当我在 Vivaldi（*基于 Chromium 的浏览器*）上测试时，网页应用商店并没有显示任何警告，但搜索扩展时的行为是相同的。

随后，我进入了谷歌浏览器扩展设置，看到了一个新的对话框。👇

![a screenshot of the ublock origin extension settings on chrome](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_b.webp)

它显示了与之前类似的警告，称该扩展可能很快就不再支持，并附有一个“查找替代品”的按钮。

![a screenshot of recommended extensions for replacing ublock origin on chrome](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_c.webp)

点击按钮后会跳转到一个 [网页](https://chromewebstore.google.com/detail/cjpalhdlnbpafiamejdnhcphjbkeiagm/related-recommendations)，其中列出了一些谷歌推荐的替代方案，其中一个名字很熟悉；稍后我会详细介绍。

当这个淘汰过程在 2025 年初完成后，**我们熟悉的谷歌浏览器上的 uBlock Origin 将不复存在**。用户将不得不切换到 [Firefox](https://www.mozilla.org/en-US/firefox/)（*或其任何衍生版*）和 [Brave](https://brave.com/) 等替代浏览器，以继续享受高级广告拦截功能。

谷歌确实提到，**在扩展程序被禁用后，用户可以重新启用它们**，但这一选项将逐步从谷歌浏览器中移除。他们还指出，使用 [ExtensionManifestV2Availablilty](https://chromeenterprise.google/policies/#ExtensionManifestV2Availability) 策略的企业用户在 2025 年 6 月之前不会受到此变更的影响。

### 不过，还有办法！😉

![a screenshot of ublock origin lite chrome web store listing](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_d.webp)

您可能已经注意到，在推荐的扩展程序页面上，**uBlock Origin Lite** 就在其中。别担心，它不是冒牌货，而是由 Raymond Hill（*gorhill*）和 uBlock Origin 团队推出的**官方版本**，并且已经获得了“*精选*”标签。

但由于 Manifest V3 的限制，**uBlock Origin Lite 是 uBlock Origin 的一个简化版**，不具备 uBlock Origin 的全部功能。

![a screenshot of ublock origin lite settings on chrome](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_e.webp)

正如上图所示，与 uBlock Origin 相比，简化版扩展的控制面板功能非常有限，用户无法添加自定义过滤器，也不能调整外观和行为。

这个扩展甚至没有元素选择器和元素清除模式，这可是对付那些试图在奇怪位置隐藏广告或弹出付费墙网站的必备功能。

但 uBlock Origin Lite 也并非完全不堪。**在我对 uBlock Origin Lite 进行测试时，使用的版本是 Chrome 127**，它成功地屏蔽了 YouTube 上的广告。对于浏览网页或流媒体等日常使用场景来说，它应该还是可以胜任的。

## 📥 获取 uBlock Origin Lite

如果想在谷歌浏览器中安装 uBlock Origin Lite，您可以从 [Chrome 应用商店](https://chromewebstore.google.com/detail/ddkjiahejlhfcafbddmgiahcphecmpfh) 中获取。

如需源代码请访问 [Github 仓库](https://github.com/uBlockOrigin/uBOL-home)，您可以在那里找到 uBlock Origin Lite 和原版 uBlock Origin 有哪些不同之处。

<center>{% button "uBlock Origin Lite" https://chromewebstore.google.com/detail/ddkjiahejlhfcafbddmgiahcphecmpfh %}</center>

我知道看到 uBlock Origin 离开谷歌浏览器是一件令人沮丧的事情，就我个人而言，到时候我会在我的谷歌浏览器上转而使用 uBlock Origin Lite（*我不会在我 Linux 电脑上使用谷歌浏览器*）。

*💬 那您呢？在淘汰完成后您还会使用谷歌浏览器吗？*
