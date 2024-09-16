---
title: 谷歌推出面向开发人员的开源人工智能代理
date: {{release_date}}
author:
  - fosscope-translation-team
  - excniesNIED
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/google-introduces-open-source-ai-agent-for-developers/google-new-project-oscar.webp
cover: https://static.fosscope.com/articles_img/2024/08/google-introduces-open-source-ai-agent-for-developers/google-new-project-oscar.webp
categories:
  - 翻译
  - 新闻
tags: 
  - 谷歌
  - AI
authorInfo: |
  via: https://news.itsfoss.com/google-ai-agent-devs/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[excniesNIED](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

谷歌是项目维护者的好帮手。

<!-- more -->

谷歌虽然在过度利用用户数据方面声名狼藉，但也长期致力于为 [开源项目](https://opensource.google/projects) 做出贡献，甚至开源 [自己的一些项目](https://news.itsfoss.com/google-open-source-tools-ai/)。

毋庸置疑，人工智能的热潮并没有被他们忽视，他们一直忙于开发新的基于人工智能的解决方案，以应对不断变化的数字环境。

最近的一个例子是，他们推出了一项名为「**奥斯卡计划（Project Oscar）**」的开源框架，用于创建基于人工智能的助手或 "代理"，以帮助软件开发和维护工作。

## 奥斯卡计划：人工智能代理的崛起？

{% video youtube:986_MUsOk1g %}

奥斯卡计划旨在提升开源软件开发的效率，它是 **一种实验性的开源贡献者代理架构**，可用于将代理部署到代码仓库中，以处理诸如接收问题、将问题与现有文档匹配等任务。

该项目的 **一些关键目标** 包括减少维护者在处理问题、变更列表、拉取请求、论坛提问等方面的工作量，并为软件的更高效维护奠定基础。

然而，该项目目前隶属于 [Go 项目](https://go.dev/project)，未来可能会也可能不会成为一个独立的项目。这并不意味着它只能与 Go 语言一起使用，开发者希望它足够灵活，以便与其他项目一起使用。

谷歌表示，他们已经确定了奥斯卡计划将具备的 **三个主要能力**：

- 利用自然语言来控制确定性工具。
- 在贡献者互动过程中索引和展示与项目相关的上下文信息。
- 审查问题报告、变更列表和拉取请求，并尝试在提交后对其进行改进。

如果你有兴趣看看奥斯卡代理的实际运作，Go 项目使用了一个基于奥斯卡的代理，名为 [Gaby](https://github.com/gabyhelp)（Go AI Bot），你可以在 Go 的 GitHub 仓库中看到它，它负责处理 [问题](https://github.com/golang/go/issues?q=label%3Agabywins&)，并以 *@gabyhelp* 的身份发帖。

### 想一探究竟吗

如前所述，奥斯卡是 Go 项目的一部分，有兴趣了解的人可以访问 [官方仓库](https://go.googlesource.com/oscar/)，在那里还能找到更多关于它如何工作的信息。

<center>{% button "奥斯卡（Oscar）" https://go.googlesource.com/oscar/ %}</center>

如果您有任何疑问，或想为奥斯卡提出一个想法，可以在 [GitHub](https://github.com/golang/go/discussions/68490) 上进行提出。
