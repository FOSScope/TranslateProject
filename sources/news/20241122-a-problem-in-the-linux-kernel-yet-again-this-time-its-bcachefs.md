---
title: "A Problem in the Linux Kernel Yet Again: This Time, It's Bcachefs!"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/11/bcachefs-linux-kernel-problem.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/11/bcachefs-linux-kernel-problem.png
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://news.itsfoss.com/linux-kernel-bcachefs/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
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

Some issues with the developer of bcachefs in the Linux Kernel community. Maybe, it's just being overblown? What do you think?

<!-- more -->

2024's been an interesting year for the Linux kernel, more so in the final months when we saw the [expulsion of Russian maintainers](https://news.itsfoss.com/russian-linux-maintainers-geopolitics/) over compliance requirements, and then a subsequent move by Russia to [build its own Linux community](https://news.itsfoss.com/russia-linux-community/).

Linux kernel development is no stranger to a few controversies here and there, but geopolitics affecting their work was a surprise indeed.

Unfortunately, something else has happened now that involves [Bcachefs](https://bcachefs.org/), the copy-on-write (COW) filesystem for Linux that focuses on reliability and being a robust alternative to ZFS and Btrfs.

## What's Going On With Bcachefs?

<img alt="a screenshot of a blog titled trouble in the kernel by kent overstreet" height="450" width="1312" />\<img src="https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_a.png" class="kg-image" alt="a screenshot of a blog titled trouble in the kernel by kent overstreet" loading="lazy" width="1312" height="450" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_a.png 600w, https://news.itsfoss.com/content/images/size/w1000/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_a.png 1000w, https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_a.png 1312w" sizes="(min-width: 720px) 720px"\>Source: [Kent Overstreet](https://www.patreon.com/posts/116412665)

Kent Overstreet, the creator of Bcachefs, has put out [a blog](https://www.patreon.com/posts/116412665) detailing **how the future of Bcachefs in the Linux kernel looks uncertain**, as Linus Torvalds has rejected a pull from him for the upcoming Linux 6.13, citing “*an open issue with the CoC board*”.

If you didn't know, the Linux kernel CoC committee (*mentioned as “board” above*) is tasked with enforcing the [Code of Conduct](https://docs.kernel.org/process/code-of-conduct.html) (*CoC*) that applies to the project, both in project spaces and in the public. The latter is applicable when an individual is publicly representing the project or the community as a whole, including on social media or online/offline events.

The consensus is that a recent [offensive reply](https://lore.kernel.org/all/citv2v6f33hoidq75xd2spaqxf7nl5wbmmzma4wgmrwpoqidhj@k453tmq7vdrk/) (*back in September*) by Kent to Linux [memory management](https://www.kernel.org/doc/html/v5.1/admin-guide/mm/index.html) (MM) developer, [Michal Hocko](https://lwn.net/Articles/684487/) is behind the suspension. As you can see below, Kent was not happy with how Michal was handling things related to *PF\_MEMALLOC\_NORECLAIM*.

<img alt="" height="518" width="652" />\<img src="https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_b.png" width="652" height="518" loading="lazy" alt="" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_b.png 600w, https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_b.png 652w"\>

<img alt="" height="358" width="612" />\<img src="https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_c.png" width="612" height="358" loading="lazy" alt="" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_c.png 600w, https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_c.png 612w"\>

The offending reply by Kent Overstreet and a following post by Shuah Khan.

In subsequent replies, Kent was asked by [Shuah Khan](https://www.linkedin.com/in/shuah-khan/) of the Linux kernel CoC committee to not use such language, and to adhere to the Code of Conduct. To that, Kent responded that he had [worked this out](https://lore.kernel.org/all/vvulqfvftctokjzy3ookgmx2ja73uuekvby3xcc2quvptudw7e@7qj4gyaw2zfo/t/) with Michal privately, with the CoC committee receiving the copies of the interactions.

However, Shuah [didn't let it go](https://lore.kernel.org/all/vvulqfvftctokjzy3ookgmx2ja73uuekvby3xcc2quvptudw7e@7qj4gyaw2zfo/t/), asserting that he had to apologize. Consequently, there has been plenty of discussion over this, with Kent refusing to apologize publicly.

## What Happens Now?

<img alt="a screenshot of the formalized coc enforcement policy for linux kernel being announced on lore.kernel.org" height="784" width="762" />\<img src="https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_d.png" class="kg-image" alt="a screenshot of the formalized coc enforcement policy for linux kernel being announced on lore.kernel.org" loading="lazy" width="762" height="784" srcset="https://news.itsfoss.com/content/images/size/w600/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_d.png 600w, https://news.itsfoss.com/content/images/2024/11/Bcachefs\_Linux\_Kernel\_-fiasco\_d.png 762w" sizes="(min-width: 720px) 720px"\>

All of this seems to have been taken up a notch by the [formalized CoC enforcement policy](https://lore.kernel.org/lkml/20241114205649.44179-1-skhan@linuxfoundation.org/) that was published on November 14, 2024. It expands on what kind of actions might be taken in cases of unacceptable behavior.

There are **provisions on it that can be used against offenders**. With a public apology by the offender being the first one. If an offender doesn't do that, then a ban from participating in kernel development, either for a short period or a full kernel development cycle, could be handed out.

In such a case, the offender may be required to publicly apologize to get back in, but that is not a mandatory requirement. The CoC committee has the final say in that.

Kent's blog appeared a few days after the publishing of the policy, so it looks like this is likely to be a drawn-out dispute. In the blog, he goes on to share that **his reply was not meant to be malicious or personal**, and things like this happen when developers get into technical arguments.

As for the CoC's handling of the situation (*via Shuah*), many Linux kernel maintainers, including Kent, are unhappy with how heavy-handed the interactions have been, with CoC enforcement also being brought into question.

If you are interested in reading the ongoing conversation surrounding this, then you can go through the [original thread](https://lore.kernel.org/all/vvulqfvftctokjzy3ookgmx2ja73uuekvby3xcc2quvptudw7e@7qj4gyaw2zfo/t/) that is at the core of it all.

In the end, some questions remain: *What will happen to the Bcachefs implementation in the mainline Linux kernel? Will it stay or go away? Is this a temporary suspension for Kent Overstreet, or a more permanent one?*

For answers to all that, we have to wait and see what happens.

*💬 Tell me what you think of this situation in the comments below!*
