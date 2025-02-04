---
title: Hyprland 0.47.0 Releases with HDR Support and Squircles
date: {{release_date}}
abbrlink: 
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - 新闻
tags: 
  - {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/hyprland-0-47-0-release/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesnied](https://github.com/excniesnied)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

You will notice many handy changes with this Hyprland release, from rounded window edges to the introduction of HDR support.

<!-- more -->

Hyprland is the most popular up-and-coming dynamic tiling window compositor out there. It has quickly gained an ardent following of users who prefer its eye candy potential over boring desktop environments, alongside the massive gains in performance and efficiency on Wayland sessions.

Even though it is far from a stable 1.0 release, its current lineup of releases is a solid choice for those looking to rice their Linux setups.

Recently, in an announcement made by the lead developer of Hyprland, a new point release, 0.47.0, has been introduced. Let's dive into it. 😄

## 🆕 Hyprland 0.47.0: What's New?

{% image https://news.itsfoss.com/content/images/2025/01/Hyprland_Banner.png '' %}

Right off the bat, we have the **newly added support for squircles** (_rounded edges_) for windows, bringing Hyprland on par with what many others offer. Next up is the **addition of experimental HDR and color management support** , which was a much-needed feature for improving visual quality and accuracy, especially for those with high-end displays.

Then comes the implementation of _hyprland_surface_ and _hyprland_lock_notify_ , which improve the behavior of screen locking and system suspend.

{% image https://news.itsfoss.com/content/images/2025/01/Hyprland_Donation_Request.png '' %} {% image https://news.itsfoss.com/content/images/2025/01/Hyprland_Squircles.png 'Screenshots of Hyprland 0.47.0\'s squircles and donation request dialog. (Source: <a href="https://github.com/vaxerski/?ref=news.itsfoss.com">Vaxry</a>)' %}

Similar to KDE, Hyprland now features a “donation nag”—**a donation prompt that will appear twice a year, in July and December** , to remind users to donate and help keep the project in top shape.

_There is a command to disable this behavior, but I won't mention it._ 😠

We conclude this with some miscellaneous changes:

  * Fix for XWayland cursor glitching.
  * There is now support for GPU hotplug.
  * A new option to force reload all plugins in hyprpm.
  * Smoother transition for CTM (_used in hyprsunset_), except on NVIDIA hardware.

You can learn more about this release by going through the announcement blog.

## 📥 Get Hyprland 0.47.0

The lead developer has stopped pushing out binary releases, so those who want to get started with this Hyprland release will have to build from source. Files can be found on GitHub.

{% button 'Hyprland 0.47.0' 'https://github.com/hyprwm/Hyprland/releases/tag/v0.47.0' %}

If you're looking to install Hyprland on your Linux system, be sure to check out our comprehensive guide. We've covered installation steps for all the popular distros, making it easy for you to get started.
