---
title: Netflix 开源其秘诀以满足平台需求
date: {{release_date}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/netflix-open-sources-its-secret-sauce-to-meet-the-demands-of-its-platform/netflix-opensource-maestro.webp
cover: https://static.fosscope.com/articles_img/2024/08/netflix-open-sources-its-secret-sauce-to-meet-the-demands-of-its-platform/netflix-opensource-maestro.webp
categories:
  - 翻译
  - 新闻
tags: 
  - Netflix
  - 开源
authorInfo: |
  via: https://news.itsfoss.com/netflix-maestro-open-source/

  作者：[Ankush Das](https://news.itsfoss.com/author/ankush/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true
translated: true
proofread: false
published: false
---

Netflix 押注开源！

<!-- more -->

每家公司都依赖于某种形式的工作流程组织，他们设计出一种机制或工具，帮助他们最大限度地利用资源，满足客户需求，方便软件开发等。

不仅仅是 Netflix 这样的大公司，每家公司都有自己独特的问题和处理问题的思路。 因此，这里没有一刀切的解决方案。

然而，如果一家公司投入大量资金来构建自己的工作流引擎，然后他们将其开源，这是个好消息！ 🥳

## 认识一下 Netflix 的工作流协调器「Maestro」

![netflix maestro](https://static.fosscope.com/articles_img/2024/08/netflix-open-sources-its-secret-sauce-to-meet-the-demands-of-its-platform/netflix-opensource-maestro.webp)

如果你是云计算爱好者，那么「协调器」这个词可能会让你联想到 Kubernetes 或微服务。 但是，Maestro 并非如此。

正如官方博客所描述的：

> *Maestro 是一款通用、可横向扩展的工作流协调器，旨在管理大规模工作流，如数据管道和机器学习模型训练管道。*

Netflix 等公司需要收集数据、处理数据、存储数据、转换数据、验证数据并监控数据。 任何与数据工程有关的工作都涉及同样的流程。

换句话说，向您推荐您最喜欢的节目、分析哪些最有效、哪些无效、管理媒体以及任何后端技巧，一切都是数据驱动的（大量数据）。 而使用这样的工具就能为这一切提供便利。

可以说，Maestro 是 Netflix 平台的核心，它使所有齿轮同步工作，让工程师工作起来得心应手，让合作伙伴获得所需的所有见解，让客户无缝访问服务。

Netflix [在 2022 年推出 Maestro](https://netflixtechblog.com/orchestrating-data-ml-workflows-at-scale-with-netflix-maestro-aaa2b41b800c) 以解决可扩展性问题之前，曾使用 Meson（另一种协调器）。 但是，它并没有开源。

现在，Netflix 似乎相信自己的解决方案可以帮助他人，并利用开源社区的帮助进一步改进它。 因此，他们决定开源整个代码，并以 **Apache 2.0 许可证**在 [GitHub](https://github.com/Netflix/maestro) 上发布。


<center>{% button "Maestro GitHub" https://github.com/Netflix/maestro %}</center>

在 [Hacker News 的讨论](https://news.ycombinator.com/item?id=41037745&) 中，一些用户似乎认为这纯粹是公关行为，既然有 [Apache Airflow](https://airflow.apache.org/) 这样的选择，他们就没必要重新发明轮子。

有些人怀疑 Netflix 是否会继续使用它，或者以后放弃它，转而使用其他技术，比如 [Conductor](https://github.com/Netflix/conductor)（Netflix 的老技术）。

另一些人则认为这是一个好举措，可以帮助开源社区根据不同的业务逻辑重新利用代码。

我不是数据工程师，所以不知道这与现有解决方案相比在技术上有何优势。 因此，我想让你从他们 [详细的公告博文](https://netflixtechblog.com/maestro-netflixs-workflow-orchestrator-ee13a06f9c78) 中找到答案。

*💭您如何看待 Netflix 将其最新工作流引擎开源的决定？ 请在下面的评论中告诉我您的想法！*
