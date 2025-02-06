---
title: 我最近测试的 10 款基于人工智能的搜索引擎
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/06/ai-search-engines.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/06/ai-search-engines.png
categories:
  - 翻译
  - 技术
tags: 
  - AI
  - 搜索引擎
authorInfo: |
  via: https://itsfoss.com/ai-search-engines

  作者：[Community](https://itsfoss.com/author/community/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[Churnie HXCN](https://github.com/excniesnied)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

没人对现状感到满意，但它们已经出现了。为了一探究竟，我们来看看一些人工智能搜索引擎的选择。

<!-- more -->

为了整理出最相关的答案而浏览多个网站，这往往令人厌烦。于是，像谷歌（Google）和必应（Bing）这样的搜索引擎应运而生。当然，它们可能不太注重隐私保护，但它们改变了我们在网络上搜索信息的方式。

现在，我们有众多选择，包括 [注重隐私的搜索引擎](https://itsfoss.com/privacy-search-engines/)，而且它们一直在不断发展，具备了各种功能，其中就包括将人工智能与搜索引擎相结合。

**有了基于人工智能的搜索引擎，搜索体验发生了改变**。

但这些人工智能搜索引擎真的值得你花费时间吗？还是说它们是一把双刃剑？

在亲自试用了几款这样的搜索引擎后，我写下了自己的想法，以回答这个问题，并帮助你决定哪款基于人工智能的搜索引擎最值得一试。

## **什么是人工智能搜索引擎？它更好吗？**

与基于预定义算法和关键词匹配运行的传统搜索引擎不同，**人工智能搜索引擎利用自然语言处理（NLP）和深度学习**为你提供搜索结果的总结。

搜索引擎确实已经能为你提供相关答案，但借助**自然语言处理算法**它会尝试从众多可能的答案中找出**最佳答案**。

由人工智能驱动的搜索引擎使用了大语言模型（LLM），这让你可以**通过聊天机器人进行对话交互**，在某些情况下，还能为你**生成文本**或**总结**结果。

{% video youtube:s4InWsd-J6g width:100% autoplay:0 %}

因此，使用具备人工智能功能的搜索引擎，你可以期待获得以下好处：
- **获取搜索内容的总结信息**
- **获得针对你研究的高度具体的建议**
- **在搜索时使用额外的工具（如笔记、聊天功能）**

然而，这些由人工智能驱动的搜索引擎往往会给出令人存疑的结果。在一个广泛流传的例子中，**谷歌的人工智能概述**模仿了一条 Reddit 评论，建议 *用胶水把奶酪粘在披萨上* 🍕。这可能是因为谷歌在其人工智能模型的训练中使用了Reddit的内容 💀

因此，尽管这些 **人工智能搜索引擎可能会为你节省大量时间，但你也需要核实它们提供的所有信息，这使得它们成为一把双刃剑**。

既然你已经了解了人工智能搜索引擎的注意事项 ⚠️ 和好处 ✅，让我来列举一些你可以尝试的选项。

{% note color:yellow ✋ ***\*非自由开源软件警告！\**** 这里提到的大多数选项本质上都不是开源的。这只是对 Linux 网络用户的一个推荐。我们与这些选项没有任何关联。 %}

## 1. Perplexica

![perplexica](https://itsfoss.com/content/images/2024/06/perplexica-screenshot.png)

Perplexica是一款开源的人工智能搜索引擎，旨在作为Perplexity AI（下面会提到的一款专有搜索引擎）的替代方案。它会在搜索网络的同时引用来源，并提供简洁的信息。

Perplexica的核心采用了 [SearxNG](https://github.com/searxng)，这是一款自由开源的元搜索引擎。它允许你在本地使用诸如 Llama 3 和 Mixtral 等大语言模型。这款搜索引擎提供了三种模式：Copilot 模式、普通模式和专注模式。Copilot 模式应该是一种高级模式，目前仍在开发中。

专注模式提供了六种不同的搜索模式（*这是我很喜欢的一点！*）。当我遇到一个数据分析问题时，该模式允许我进行「**Wolfram Alpha**」搜索，它可以解决所有与计算和数据相关的查询。

Perplexica完全免费，仅依靠捐赠维持运营。你可以选择将其部署在云端，也可以在本地机器上运行。

**主要亮点：**

{% note color:cyan ✅ 开源 ✅ 可自行部署 ✅ 支持本地大语言模型 ✅ 可连接网络 ✅ 答案会引用来源 ⚠️ 正在积极开发中 %}

<center>{% button "Perplexica" https://github.com/ItzCrazyKns/Perplexica %}</center>

## 2. Perplexity AI

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-131947.png)

Perplexity是一款**用于研究目的的有趣的人工智能搜索引擎**。它采用**免费增值模式**，使用了**Anthropic公司的 Claude 3 Haiku 模型**以及**该公司自己的大语言模型**（LLM）。

「专注」功能允许用户将搜索范围过滤到 Reddit、YouTube 或学术资源，这可能会使搜索更加高效。我喜欢 Perplexity AI 的一点是，它**像维基百科一样会引用来源**，这对于任何想要核实信息的人来说都是一件好事。

{% video youtube:QfoulVr6UU8 width:100% autoplay:0 %}

虽然 Perplexity 可以免费使用，但每月支付 **20 美元**可以升级到 Perplexity Pro 版本，从而获得对 GPT - 4、Claude 3、Mistral Large、Llama 3 以及他们大语言模型实验版本的访问权限。此外，付费版本还允许你上传图片并分析文件。

**主要亮点：**

{% note color:cyan ✅ 适合研究目的 ✅ 答案会引用来源 ⚠️ 不开源 %}

<center>{% button "Perplexity AI" https://www.perplexity.ai/ %}</center>

## 3. You.com

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132029.png)

「搜索的未来」是用来描述 You.com 的词汇。虽然它可能已经发展成为一个人工智能助手，但它仍然保留着作为一个注重个性化的搜索引擎的能力。

我喜欢它可以灵活切换各种领先的人工智能模型，比如 OpenAI 的 GPT - 4、Anthropic 的 Claude 系列等等。不过，你需要注册一个免费账户才能访问更多模型，这有点麻烦，但事实就是如此。

You.com 是免费的，但每月支付 **15 美元**可以让你获得更多大语言模型的选择，还能上传媒体进行搜索，并提供更多的个性化选项。我发现的唯一缺点是，You.com 更像是一个聊天式的助手，而不太像传统的搜索引擎。

**主要亮点：**

{% note color:cyan ✅ 可以灵活选择你喜欢的人工智能模型 ⚠️ 需要注册才能尝试更多人工智能模型 %}

<center>{% button "You.com" https://you.com/ %}</center>

## 4. DuckDuckGo AI Chat

![duckduckgo ai chat](https://itsfoss.com/content/images/2024/06/duckduckgo-ai-chat.png)

DuckDuckGo 是最注重隐私的搜索引擎之一，它比其他竞争对手更鼓励采用开源解决方案。它的隐私扩展程序和浏览器应用程序都是开源的。

它不会在搜索结果中加入人工智能总结。不过，它有一个「**AI Chat**」功能，这是 ChatGPT 的一个私密版本。在这里，你可以选择一些 [开源大语言模型](https://itsfoss.com/open-source-llms/) 来提升你的聊天体验，这使它成为一个不错的选择。

**主要亮点：**

{% note color:cyan ✅ 注重隐私的选项 ✅ 可以使用开源大语言模型 ✅ 完全免费 ⚠️ 正在积极开发中（测试版）%}

<center>{% button "DuckDuckGo AI Chat" https://duckduckgo.com/?q=DuckDuckGo&ia=chat&atb=v426-1 %}</center>

**推荐阅读 📖**

{% link https://itsfoss.com/open-source-llms/ 14 款用于研究和商业用途的顶级开源大语言模型 icon:https://itsfoss.com/content/images/2024/05/open-source-llms.png %}

## 5. Bing AI 或 Microsoft Copilot

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132404.png)

由微软（Microsoft）提供支持的必应（Bing）经过多年的发展，具备人工智能功能后曾被称为「Bing Chat」。现在它终于达到了稳定状态，成为了一个可靠且智能的搜索引擎。它由 **OpenAI 的 GPT-4 模型**驱动，后来更名为 Copilot，由它来完成人工智能方面的主要工作。

一个额外的好处是，它免费提供了一个人工智能图像生成器。这个生成器基于 **DALL-E 模型**。然而，它因过于敏感而受到批评，用户可能会因为一些非常随意的提示而被封禁。

搭载 Copilot 的必应免费提供所有功能，这是它最大的优点之一。你可以付费升级到 Copilot 高级版，以获得更快的响应速度，并与微软的应用程序进行集成。

<center>{% button "Bing AI" https://www.bing.com/chat %}</center>

**主要亮点：**

{% note color:cyan ✅ 免费的人工智能图像生成器 ✅ 与谷歌相比，用户体验更简洁 ✅ 可与微软 Edge 浏览器集成 ⚠️ 依赖 OpenAI 的 ChatGPT %}

## 6. Brave Search

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132450.png)

搜索引擎以跟踪和记录用户数据而闻名，而 [Brave Search](https://search.brave.com/) 在这方面脱颖而出。它提供了**首款注重隐私保护的**搜索引擎。

Brave 的人工智能会为你的查询提供解决方案，并引用所有来源。我喜欢 Brave 人工智能用项目符号呈现信息的方式。而且，与谷歌的人工智能相比，它会在总结下方直接显示搜索结果，不会添加其他元素。

与大多数其他搜索引擎不同，Brave 拥有独立的搜索引擎，并自行托管大语言模型以保护隐私。

Brave Search 的人工智能功能完全免费。不过，如果你想在浏览器中使用 Brave 的 Leo AI 助手，可以选择付费的高级版本。

<center>{% button "Brave Search" https://search.brave.com/ %}</center>

**主要亮点：**

{% note color:cyan ✅ 注重隐私的搜索引擎  ✅ Brave 自行托管大语言模型，以更好地控制隐私 ✅ 可与 Brave 网络浏览器集成 ⚠️ 尽管 Brave 有开源的历史，但它并非开源 %}

**推荐阅读 📖**

{% link https://itsfoss.com/brave-search-features/ Brave Search的10个令人惊叹的功能值得关注 icon:https://itsfoss.com/content/images/2023/05/brave-features.png %}

## 7. Komo AI

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132530.png)

[Komo](https://komo.ai/) 提供了一种简洁的体验，旨在满足不同用户的需求。

Komo 使用自己训练的数据，能够为我的查询提供大量信息。它还会在查询下方提供更多相关问题，帮助我找到关于该主题的更多信息。我发现一个有趣的功能是「**观点**」，它会从其他来源提供与问题相关的更多信息。

Komo 的部分服务是免费的。你可以选择每月 **8 美元**的基础套餐，该套餐允许你无限制地获取社区中的人类观点；每月支付 **15 美元**则可以获得更多的自定义选项。

**主要亮点**：

{% note color:cyan ✅ 使用自己的数据集进行训练 ✅ 针对你的查询提供后续问题和更相关的问题 ⚠️ 加载速度慢 ⚠️ 某些搜索结果的语气奇怪 %}

<center>{% button "Komo AI" https://komo.ai/ %}</center>

## 8. Phind

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132608.png)

[Phind](https://www.phind.com/) 是一款专门为开发者设计的智能搜索引擎，专注于解决技术查询问题。

它基于亚马逊网络服务（AWS）开发，利用亚马逊弹性计算云（Amazon EC2）作为后端。我使用 Phind 来解决各种编程问题，它给出的答案相当不错。你还可以获得代码片段建议，并将其复制到剪贴板。

Phind 的专业版每月收费 **17 美元**，它可以增加上下文长度，并提供更多福利。此外，在训练其聊天机器人时，它不会使用你的数据，还能分析图像。

**主要亮点：**

{% note color:cyan ✅ 专注于解决开发者的问题 ✅ 可与VS Code集成 ⚠️ 搜索几次后需要注册 %}

<center>{% button "Phind" https://www.phind.com/ %}</center>

## 9. Google Gemini

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132657.png)

尽管我们之前提到过谷歌的人工智能会给出一些非常不准确的搞笑结果，但 [Google Gemini](https://gemini.google.com/app) 在某些搜索中确实能提供相当准确的结果。

如果你使用的是安卓手机，它应该是一个不错的选择，它可以增强或取代谷歌的传统助手。 Google Gemini 允许你将其与包括地图、酒店、YouTube、音乐等在内的服务进行集成。

![google search with AI.](https://itsfoss.com/content/images/2024/06/google-search-ai.png)

你可以使用 Google Gemini 人工智能，也可以通过 [搜索实验室的实验性功能](https://labs.google.com/search) 在谷歌搜索引擎上启用人工智能，如上图所示。

你可以选择付费套餐，每月支付 **19.99 美元**即可访问 Gemini Advanced 版本，并享受 Google One 的福利，如 **2 TB存储空间**等。

**主要亮点：**

{% note color:cyan ✅ 对于使用谷歌服务的用户来说非常不错 ✅ 可以与其他谷歌服务进行集成 ⚠️ 考虑到谷歌可以获取的大量数据，有时结果的不准确程度令人惊讶 %}

<center>{% button "Google Gemini" https://gemini.google.com/app %}</center>

## 10. Yep

![img](https://itsfoss.com/content/images/2024/06/Screenshot-2024-06-10-132734.png)

Yep 提供了一种公正、私密的搜索体验，并会对内容创作者进行奖励和补偿。我将它列入其中是因为它是由 **Ahref**（一家知名的 SEO 工具公司）打造的有趣选项之一。

虽然它的搜索结果不会用人工智能进行总结，但它提供了一个 AI Chat 功能，当你需要时，可以快速与聊天机器人交互以获取信息。

Yep 的搜索引擎完全免费提供所有服务。

**主要亮点：**

{% note color:cyan ✅ 旨在奖励内容创作者 ✅ 以 SEO 为重点，是谷歌的一个不错替代选项 ⚠️ AI 聊天功能正在积极开发中 %}

<center>{% button "Yep" https://yep.com/ %}</center>

## 搜索引擎被颠覆了吗？是与否

人工智能搜索引擎可能还不够完美，但它们确实比以往任何时候都更接近理想状态。随着**机器学习**的不断发展，用不了多久，这些人工智能功能就能为我们提供近乎完美的结果，从而节省我们的时间。

当然，它们也存在很多需要注意的地方。因此，公司有必要将这些功能设为可选，或者让用户可以自行开启或关闭，而不是将其作为默认体验。

💬 *你对人工智能搜索引擎有什么看法？请在下方分享你的想法！*