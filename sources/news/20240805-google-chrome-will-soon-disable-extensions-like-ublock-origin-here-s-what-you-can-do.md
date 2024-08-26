---
title: Google Chrome Will Soon Disable Extensions like uBlock Origin: Here's What You Can Do!
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/google-phase-out-manifest-3.png
cover: https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/google-phase-out-manifest-3.png
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
---

Google Chrome is gearing up for Manifest v3 by phasing out legacy extensions.

<!-- more -->

Love it or hate it, [Google Chrome](https://www.google.com/chrome/) is **the most used web browser in the world**, be it desktop or mobile. For users on desktop, they have the added benefit of having support for extensions to further extend what Chrome can do for them.

Lately, if you have been reading the news, you must have come across how Google is sunsetting [Manifest V2](https://developer.chrome.com/docs/extensions/mv2) extensions, making way for Manifest V3 one which are supposed to be a step towards improving privacy, security, and performance.

As for what a Manifest is, it's a [JSON file](https://developer.chrome.com/docs/extensions/reference/manifest) that accompanies an extension which the browser can read to get important information like its name, version number, what permissions it needs, and more.

In line with their Manifest V2 [phaseout plans](https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline), the developers shared [earlier](https://blog.chromium.org/2024/05/manifest-v2-phase-out-begins.html) this year that Chrome will begin the phaseout process in June 2024, starting with the *Beta*, *Dev*, and *Canary* channels of Chrome.

They already removed the “*Featured*” badge for Manifest V2 apps on the [Chrome Web Store](https://chromewebstore.google.com/), with uBlock Origin being one of the more popular ones being affected.

And, they aren't stopping there. Users of [uBlock Origin](https://github.com/gorhill/uBlock) might want to continue reading.

## End of uBlock Origin On Chrome? 😨

![a screenshot of the ublock origin extension listing on the chrome web store with a warning](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_a.png)

Yes, and no. You see, Google Chrome has now started showing a warning on the Chrome Web Store [listing](https://chromewebstore.google.com/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm) for uBlock Origin that says:

> This extension may soon no longer be supported because it doesn't follow best practices for Chrome extensions.

Plus, when searching for it, the store doesn't show it on the top of the search results in the search bar, but does show it at the top of the search results page.

When I tested this on Vivaldi (*a Chromium browser*), there was no warning shown on the web store, but the search behavior was the same.

I then went into the extension settings for it on Chrome, and saw a new dialog being shown. 👇

![a screenshot of the ublock origin extension settings on chrome](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_b.png)

It showed me a similar warning as before saying that this extension may soon no longer be supported, with a button to “*Find alternative*”.

![a screenshot of recommended extensions for replacing ublock origin on chrome](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_c.png)

After clicking on that, I was taken to [a webpage](https://chromewebstore.google.com/detail/cjpalhdlnbpafiamejdnhcphjbkeiagm/related-recommendations) which listed some alternatives that Google recommends, with a familiar name in the mix; More on that later.

When this phaseout is complete by the start of 2025, **uBlock Origin on Chrome as we know it will cease to exist**. Users will have to switch to alternatives like [Firefox](https://www.mozilla.org/en-US/firefox/) (*or any of its derivatives)* and [Brave](https://brave.com/) to take advantage of the advanced ad-blocking capabilities.

Google does mention that **after the extensions are disabled, they can be re-enabled by users**, but that option will be gradually removed from Chrome. They also point out that Enterprises using the [ExtensionManifestV2Availablilty](https://chromeenterprise.google/policies/#ExtensionManifestV2Availability) policy will be unaffected by this change until June 2025.

### However, There's Still a Way! 😉

![a screenshot of ublock origin lite chrome web store listing](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_d.png)

As you might have noticed earlier in the recommended extensions page, **uBlock Origin Lite** is one of the options. Don't worry, it's **not an impostor, but an official offering** by Raymond Hill (*gorhill*) and the uBlock Origin team that has already received the “*Featured*” tag.

But, thanks to the limitations of Manifest V3, **uBlock Origin Lite is a stripped down version of uBlock Origin**, that doesn't feature all the firepower of the latter.

![a screenshot of ublock origin lite settings on chrome](https://static.fosscope.com/articles_img/2024/08/google-chrome-will-soon-disable-extensions-like-ublock-origin-here-s-what-you-can-do/Chrome_ManifestV2_Phaseout_e.png)

As you can see above, the Dashboard for the lite extension is quite lacking when compared to uBlock Origin, which lets users add custom filters, tweak the appearance and behavior.

The extension doesn't even have element picker and zapper modes, which is a must for those pesky websites that try to hide ads in weird places, or pop-up a paywall.

But, it's not all bad. **When I tested uBlock Origin Lite on Chrome 127**, it was able to block ads on YouTube successfully. It should be fine for casual use cases such as browsing or streaming.

## 📥 Get uBlock Origin Lite

If you want to install it on your Chrome installation, then you can get it from the [Chrome Web Store](https://chromewebstore.google.com/detail/ddkjiahejlhfcafbddmgiahcphecmpfh).

Those seeking the source code can go to its [GitHub](https://github.com/uBlockOrigin/uBOL-home) repo, where they will also find what else [makes it different](https://github.com/uBlockOrigin/uBOL-home/wiki/Frequently-asked-questions-(FAQ)) from the OG uBlock Origin.

<center>{% button "uBlock Origin Lite" https://chromewebstore.google.com/detail/ddkjiahejlhfcafbddmgiahcphecmpfh %}</center>

I know it's a bummer to see uBlock Origin go away from Chrome, and personally speaking, I will be switching to uBlock Origin Lite on my Chrome installation on Windows (*I don't use it on my Linux PC*) when the time comes.

*💬 What about you? Will you use Chrome after the phaseout is complete?*
