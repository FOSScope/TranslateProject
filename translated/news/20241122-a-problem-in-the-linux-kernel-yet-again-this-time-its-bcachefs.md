---
title: "Linux 内核再出问题！这次是 Bcachefs！"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - Cubik65536
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/12/linux-kernel-bcachefs/bcachefs-linux-kernel-problem.webp
cover: https://static.fosscope.com/articles_img/2024/12/linux-kernel-bcachefs/bcachefs-linux-kernel-problem.webp
categories:
  - 翻译
  - 新闻
tags:
  - Linux
  - Linux 社区
  - Linux 内核
  - bcachefs
authorInfo: |
  via: https://news.itsfoss.com/linux-kernel-bcachefs/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[Cubik65536](https://github.com/Cubik65536)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

Linux 内核社区内的 bcachefs 开发者出现了一些问题。或许情况只是被夸大了？你怎么看？

<!-- more -->

2024 年对 Linux 内核社区来讲是个有趣的一年，尤其是在年底的几个月里，我们看到了 [俄罗斯维护者由于监管要求被移除](https://news.itsfoss.com/russian-linux-maintainers-geopolitics/)，随后俄罗斯又 [建立了自己的 Linux 社区](https://news.itsfoss.com/russia-linux-community/)。

Linux 内核开发并不乏一些争议，但地缘政治影响到他们的工作却是一个惊喜。

不幸的是，一些涉及到了 [Bcachefs](https://bcachefs.org/)，一个适用于 Linux 、旨在可靠性并提供一个 ZFS 和 Btrfs 的可靠替代方案的写入时复制（copy-on-write, COW）文件系统，发生了。

## Bcachefs 发生了什么？

{% image https://static.fosscope.com/articles_img/2024/12/linux-kernel-bcachefs/Bcachefs_Linux_Kernel_-fiasco_a.png "由 Ken Overstreet 撰写，标题为 Trouble in the kenel 的博客文章截图" %}

> 截图翻译：
>
> ### 内核中的麻烦
>
> 简述：bcachefs在内核中的未来尚不明朗，许多方面的情况都不太乐观。
>
> Linus 表示他不会接受我的 6.13 版本拉取请求，理由是"存在尚未与行为准则委员会解决的问题"。就此而言，我目前完全不清楚行为准则委员会的进展如何。我个人认为，关于我们的文化和工作方式，确实存在一些需要提出和解决的问题，但这些问题一直没有得到任何进展 - 这就是我发这篇文章的原因。
> 接下来将会是对一些（非典型的）Linux 内核维护邮件列表（Linux Kernel Mailing List，LKML）内争议的描述，以及对问题根源的分析 —— 包括文化问题和流程缺陷。
> 注意：我不希望因此而让任何人收到仇恨邮件，特别是相关的开发人员。在我看来，行为准则流程确实有一些需要改变的地方，但让我们尽量保持建设性的态度。
> 社区中的大多数人都很优秀：我作为Linux内核工程师已有超过15年的经验，遇到过许多出色的人才，我与接触到的大多数人共事都很愉快。但是在某些子系统中，我完成了一些基础性的工作，却因为这类问题而无法继续推进工作，现在这种情况又再次发生，是时候说出来了。
>
> 创作人：Kent Overstreet
> 正在开发 bcachefs —— 下一代 Linux 文件系统
>
> 来源：[Kent Overstreet](https://www.patreon.com/posts/116412665)

Kent Overstreet，Bcachefs 的开发者，发布了 [一篇博客](https://www.patreon.com/posts/116412665) 详细讲述**为什么 Bcachefs 在 Linux 内核中的未来前景尚不确定**，因为 Linus Torvalds 以"存在尚未与行为准则委员会解决的问题"为由，拒绝了他针对即将发布的 Linux 6.13 版本提交的代码合并请求。

如果你不知道的话，Linux 内核行为准则委员会的职责是执行适用于该项目的 [行为准则](https://docs.kernel.org/process/code-of-conduct.html)。这些准则的执行范围包含两个方面：项目内部空间以及公共场合。其中，关于公共场合的规定主要适用于以下情况：当个人在公开场合代表项目或整个社区时，包括在社交媒体平台或在线/线下活动中的表现。

普遍认为，这次暂停的原因是 Kent 在9月份对 Linux [内存管理](https://www.kernel.org/doc/html/v5.1/admin-guide/mm/index.html) 开发者 [Michal Hocko](https://lwn.net/Articles/684487/) 发表的一条 [具有冒犯性的回复](https://lore.kernel.org/all/citv2v6f33hoidq75xd2spaqxf7nl5wbmmzma4wgmrwpoqidhj@k453tmq7vdrk/)。从下文可以看出，Kent 对于 Michal 处理 *PF_MEMALLOC_NORECLAIM* 相关事务的方式表示不满。

{% image https://static.fosscope.com/articles_img/2024/12/linux-kernel-bcachefs/Bcachefs_Linux_Kernel_-fiasco_b.webp %}
{% image https://static.fosscope.com/articles_img/2024/12/linux-kernel-bcachefs/Bcachefs_Linux_Kernel_-fiasco_c.webp "Kent Overstreet 发表的冒犯性回复与 Shuah Khan 发布的跟进邮件" %}

> 截图翻译：
>
> > 我不是你的助手，不用接收你的任务去搜索 lore 归档。
> > 如果你需要的话自己去找一个。
> >
> > 不管怎样，如果你读了这封邮件，并且真的试图去理解其中的内容，而不是立即开始大声回应的话，你就会注意到我在这里提出了实际的论据。你可以不同意这些论据并提出你的观点。但你选择了
> >
> > \[...\]
> >
> > > 是的，我受够了这种疯狂。
> >
> > 所以我认为你无法做到这一点。再说一遍...
>
> Michal，如果你认为让进程崩溃是处理错误的可接受替代方案，那么_你就没资格编写内核代码_。
>
> 你一直在固执地为一个接一个的糟糕想法争辩，这对于我们这些关心编写可靠软件的人来说是一种侮辱。
>
> 你在反对内核编程的基本原则。
>
> 去检查一下你的脑子吧。带着这些废话从这里滚出去。
>
> <br>
> <hr>
> <br>
>
> Kent：
>
> 使用这样的语言显然是不可接受的，且违反了行为准则。这种语言无法促进相互尊重和富有成效的讨论，反而会损害社区的健康发展。
>
> 你应当清楚地认识到，这种语言方式和人身攻击明显违反了Linux内核贡献者契约行为准则，具体内容如下文所述：
>
> <https://www.kernel.org/doc/html/latest/process/code-of-conduct.html>
>
> 请参考行为准则，并在今后避免违反行为准则。
>
> 此致，
>
> -- Shuah（代表行为准则委员会）

在后续的回复中，Linux 内核行为准则委员会的 [Shuah Khan](https://www.linkedin.com/in/shuah-khan/) 要求 Kent 不要使用此类语言，并遵守行为准则。对此，Kent 回应称他已经与 Michal [私下解决了这个问题](https://lore.kernel.org/all/vvulqfvftctokjzy3ookgmx2ja73uuekvby3xcc2quvptudw7e@7qj4gyaw2zfo/t/)，并且行为准则委员会也收到了相关沟通的副本。

然而，Shuah [并未就此放过这个问题](https://lore.kernel.org/all/vvulqfvftctokjzy3ookgmx2ja73uuekvby3xcc2quvptudw7e@7qj4gyaw2zfo/t/)，坚持要求 Kent 必须道歉。因此，围绕这一事件展开了大量讨论，而 Kent 则拒绝公开道歉。

## 现在发生了什么？

{% image https://static.fosscope.com/articles_img/2024/12/linux-kernel-bcachefs/Bcachefs_Linux_Kernel_-fiasco_d.webp "Kent Overstreet 发表的冒犯性回复与 Shuah Khan 发布的跟进邮件" %}

> 截图内容翻译：
>
> 发件人：Shuah Khan skhan@linuxfoundation.org
> 收件人：gregkh@linuxfoundation.org, corbet@lwn.net
> 抄送：\[多位 Linux 内核社区重要成员和委员会成员\]
> 主题：[PATCH v4] 文档/CoC：明确规定对不可接受行为的执行措施
> 日期：2024年11月14日 13:56:49 -0700
> 消息ID：20241114205649.44179-1-skhan@linuxfoundation.org
>
> 行为准则委员会的首要目标是推动变革，确保我们的社区能够持续促进相互尊重的讨论。
>
> 为了保持透明度，现已正式确立针对不可接受行为的行为准则执行政策。
>
> 更新行为准则解释文档，加入执行相关信息。
>
> 经确认：[列出了多位 Linux 社区重要成员的确认，包括 Linus Torvalds、Greg Kroah-Hartman 等人]
> 签署：Shuah Khan <skhan@linuxfoundation.org>

所有这些事态似乎因2024年11月14日发布的 [正式行为准则执行政策](https://lore.kernel.org/lkml/20241114205649.44179-1-skhan@linuxfoundation.org/) 而进一步升级。该政策详细阐述了在面对不可接受行为时可能采取的行动措施。

这项政策包含了**针对违规者的具体条款**。其中，违规者的公开道歉是首要措施。如果违规者拒绝道歉，可能会面临针对暂时或整个内核开发周期的参与禁令。

在这种情况下，违规者可能需要公开道歉才能重返社区，但这并非强制要求。行为准则委员会对此拥有最终决定权。

Kent 的博客文章发表于该政策公布后几天，这表明这场争议可能会持续很长时间。在博客中，他解释说**他的回复并非出于恶意或针对个人**，这类情况在开发者进行技术争论时都可能发生。

关于行为准则委员会（*通过 Shuah*）对此事的处理方式，包括 Kent 在内的许多 Linux 内核维护者都对其过于强硬的处理方式表示不满，对行为准则的执行方式也提出了质疑。

如果您有兴趣了解围绕这一事件的持续讨论，可以查看位于争议核心的 [原始邮件会话](https://lore.kernel.org/all/vvulqfvftctokjzy3ookgmx2ja73uuekvby3xcc2quvptudw7e@7qj4gyaw2zfo/t/)。

最后，仍有一些悬而未决的问题：*Bcachefs 在 Linux 主线内核中的实现将何去何从？它会留存还是消失？Kent Overstreet 的封禁是暂时的还是永久的？*

要得到这些问题的答案，我们只能等待事态的进一步发展。

*💬 你对此事怎么看？在下方评论吧！*
