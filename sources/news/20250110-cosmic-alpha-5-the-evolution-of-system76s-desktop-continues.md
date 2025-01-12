---
title: "COSMIC Alpha 5: The Evolution of System76's Desktop Continues!"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/cosmic-alpha-5/

  作者：[{{author}}]({{author_link}})
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: false # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

System76's COSMIC desktop is making good progress!

<!-- more -->

The COSMIC desktop environment is taking its sweet time to be ready for a stable release, but hey, it now feels like we're waiting for Half-Life 3 at this point. I understand that great things take time, and I’m more than happy to wait.

Still, every so often, the enthusiastic nerd in me just can’t help but get a little impatient!

Not long ago, [the first Alpha release](https://news.itsfoss.com/pop-os-24-04-cosmic-alpha/) of COSMIC arrived, offering a sneak peek into the development, followed by several more Alpha releases. This time, we will explore the COSMIC Alpha 5 release. Let's see what's new. 😃

## COSMIC Alpha 5: What's Cooking?

<img alt="a screenshot of cosmic alpha 5 running on pop!_os 24.04 alpha with the fastfetch output being shown towards the right" height="1080" width="1920" />\<img src="https://news.itsfoss.com/content/images/2025/01/COSMIC\_Alpha\_5\_Fastfetch\_Output.jpg" class="kg-image" alt="a screenshot of cosmic alpha 5 running on pop!\_os 24.04 alpha with the fastfetch output being shown towards the right" loading="lazy" width="1920" height="1080" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/COSMIC\_Alpha\_5\_Fastfetch\_Output.jpg 600w, https://news.itsfoss.com/content/images/size/w1000/2025/01/COSMIC\_Alpha\_5\_Fastfetch\_Output.jpg 1000w, https://news.itsfoss.com/content/images/size/w1600/2025/01/COSMIC\_Alpha\_5\_Fastfetch\_Output.jpg 1600w, https://news.itsfoss.com/content/images/2025/01/COSMIC\_Alpha\_5\_Fastfetch\_Output.jpg 1920w" sizes="(min-width: 720px) 720px"\>

Bringing COSMIC closer to a stable version, the Alpha 5 release brings forward some fresh changes that will make it into the final release. We start off with the [COSMIC Media Player](https://github.com/pop-os/cosmic-player), which has now become **the default app for playing media on COSMIC**.

It uses [Vulkan](https://www.vulkan.org/) for rendering and [VA-API](https://en.wikipedia.org/wiki/Video_Acceleration_API) for decoding (*depending on availability*) for facilitating video playback. The developers also intend to add audio file playback and a tree view for handling audio/video files in the future.

The Variable Refresh Rate (*VRR*) implementation also sees upgrades. It now takes into account a display's minimum refresh rate to ensure that there is no jitteriness when the cursor is moved in an application that is running below the minimum refresh rate.

<img alt="" height="1008" width="1536" />\<img src="https://news.itsfoss.com/content/images/2025/01/COSMIC\_Media\_Player.png" width="1536" height="1008" loading="lazy" alt="" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/COSMIC\_Media\_Player.png 600w, https://news.itsfoss.com/content/images/size/w1000/2025/01/COSMIC\_Media\_Player.png 1000w, https://news.itsfoss.com/content/images/2025/01/COSMIC\_Media\_Player.png 1536w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="1008" width="1536" />\<img src="https://news.itsfoss.com/content/images/2025/01/COSMIC\_Alpha\_5\_Users\_Page.png" width="1536" height="1008" loading="lazy" alt="" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/COSMIC\_Alpha\_5\_Users\_Page.png 600w, https://news.itsfoss.com/content/images/size/w1000/2025/01/COSMIC\_Alpha\_5\_Users\_Page.png 1000w, https://news.itsfoss.com/content/images/2025/01/COSMIC\_Alpha\_5\_Users\_Page.png 1536w" sizes="(min-width: 720px) 720px"\>

COSMIC Media Player and Users settings page. (**Source: System76**)

The *Systems & Accounts* settings menu now has **a new Users page**, which can be used to manage all the user accounts on a system. This allows for changing the username, password, and admin permissions.

For the user interface, now *Alt+Tab* and *Super+Tab* will switch between apps in order of activity, going through the last used apps. Similarly, COSMIC Terminal can now open links; simply left-clicking on the URL should open it up with the default web browser.

There are several other notable changes as well. Some highlights include:

* Fixed compatibility with [Linux kernel 6.12](https://news.itsfoss.com/linux-kernel-6-12/).
* It is now possible to save new files in a new folder.
* Right-clicking or middle-clicking now closes context menus.
* An issue with screenshot capture on vertical monitors was addressed.

For more details, you can go through System76's [announcement blog](https://blog.system76.com/post/cosmic-alpha-5-released).

## Want To Test It Out?

The [official website](https://system76.com/cosmic/) hosts two ISO images for Intel/AMD and NVIDIA systems, both of which are running Pop!\_OS 24.04 LTS alpha.

🚧

As this is ****an under-development desktop environment****, I suggest you use it for testing and not for production/general use.

I tested it out on a [virtual machine](https://itsfoss.com/virtual-machine/), and it ran fine for the most part, but I was unable to play videos on the COSMIC Media Player.

[COSMIC Alpha 5](https://system76.com/cosmic/)
