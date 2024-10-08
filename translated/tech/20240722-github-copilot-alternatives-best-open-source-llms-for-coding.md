---
title: GitHub Copilot平替：几个最强的开源编程大模型
date: {{release_date}}
author:
  - fosscope-translation-team
  - RobertCheng-956
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - 技术
tags: 
  - Copilot
  - LLM
authorInfo: |
  via: https://itsfoss.com/coding-llms-copilot-alternatives

  作者：[Community](https://itsfoss.com/author/community/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[RobertCheng-956](https://github.com/RobertCheng-956)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

想让AT帮你敲代码？想要开源的GitHub Copilot平替编程助手？往下看看吧！

<!-- more -->

AI 无处不在。大语言模型 (LLM)就是最主流的一种AI模型。

当然，这里指的是[开源LLM](https://itsfoss.com/open-source-llms/)（而不是专有LLM）。这样的LLM不仅能帮你生成文本、活跃思维、画图创造，而且能够帮你编程，提高编写代码的效率。

为此，LLM需要首先经过微调，然后用编程语言训练，这样才能为你编程提供助力。

本篇文章中，我将介绍一些好用的开源编程LLM，其中也包含了开源的GitHub Copilot平替编程助手。

{% note color:cyan 📋 You can find all the open source LLMs on Ollama and get it installed locally without much hassle. %}

## 1. WizardCoder

![wizardcoder](https://itsfoss.com/content/images/2024/07/wizardcoder-huggingface-1.jpg)

[WizardCoder](https://github.com/nlpxucan/WizardLM)是一个开源编程大型语言模型 (LLM)，在 Llama 2的基础上进行了优化，并且经过了相应的微调，可以很好地处理复杂指令。

WizardCoder使用Evol-Instruct算法，确保模型以更完整、更丰富的指令进行微调，在编码任务中脱颖而出。得益于这一算法，该模型声称，在性能上超过了 Gemini Pro、ChatGPT 3.5等大模型。因此，WizardCoder大模型非常适合作为AI编程助手。

最新版本是**WizardCoder-33B-V1.1**，是在deepseek-coder-33b-base上训练的。您也可以使用它的变体，比如WizardCoder-Python-34B-V1.0。

如果感兴趣，可前往[Ollama](https://itsfoss.com/ollama/)库一探究竟。

<center>{% button "WizardCoder" https://huggingface.co/WizardLMTeam/WizardCoder-15B-V1.0 %}</center>

**推荐阅读📖**

{% link https://itsfoss.com/ollama-setup-linux/ Running AI Locally Using Ollama on Ubuntu Linux icon:https://itsfoss.com/content/images/2024/05/run-ai-locally-in-linux-using-ollama.png %}

## 2. Phind CodeLlama

![phind codellama](https://itsfoss.com/content/images/2024/07/phind-code-model-1.jpg)

Phind是[最好用的AI搜索引擎](https://itsfoss.com/ai-search-engines/)之一，其编程大模型也不遑多让。Phind CodeLlama是一个基于CodeLlama 34B的代码生成模型，经过微调以适应各种指令。

该模型不仅训练集中编程问题和回答质量高，还使用了DeepSpeed ZeRO 3和Flash Attention 2在32个A100-80 GB GPU上进行了3个小时的训练。

为了保证准确性，Phind利用OpenAI的去污染技术对数据集进行处理，提取每个评估用例中的部分文本，并验证训练样本中是否存在相应的匹配项。

该模型存在两个版本：v1 和 v2。v1建立在CodeLlama 34B和CodeLlama-Python 34B之上。v2版本只是 v1的迭代版本，在额外的15亿个高质量编程相关数据令牌上进行了训练。

<center>{% button "Phind CodeLlama" https://huggingface.co/Phind/Phind-CodeLlama-34B-v2 %}</center>

## 3. Mistral7B and Mixtral-8x7B

![mistral AI](https://itsfoss.com/content/images/2024/07/mistral-ai-1.jpg)

Mistral AI 开发的 Mistral7B 和 Mixtral 8x7B 都宣称自己是对应训练数据量中最好的模型。Mistral 7B 拥有 73 亿个参数，在基准测试中胜过 Llama 2 13B。

我确实发现该模型在Ubuntu系统中的Ollama上运行速度更快。

部分技术细节：Mixtral 8x7B规模更大，是一个具有467亿个参数的稀疏专家混合(SMoE)模型。尽管参数量大，但每个词元只需要129亿个参数。

这两种模型都可以根据您的任务需要进行微调。但是，也适用于编程。

<center>{% button "Phind CodeLlama" https://huggingface.co/Phind/Phind-CodeLlama-34B-v2 %}</center>

## 4. CodeBooga

![codebooga](https://itsfoss.com/content/images/2024/07/codebooga-1.jpg)

CodeBooga是一款出色的开源编程大模型，主要原因是该模型是Phind-Codellama 34B v2和WizardCoder-Python-34B-V1.0的合并结果，几乎可以说是 Python和JavaScript最佳编程模型之一。

该模型总共拥有334亿个参数，在评估其用途时可能会优于合并的模型。

CodeBooga 可能并不那么流行，但也包含在Ollama库中，可以随时尝试。

<center>{% button "CodeBooga" https://huggingface.co/oobabooga/CodeBooga-34B-v0.1 %}</center>

## **5. Code Llama**

![codellama](https://itsfoss.com/content/images/2024/07/codellama-1.jpg)

由Meta AI开发的[Code Llama](https://github.com/facebookresearch/codellama)是Llama 2的一个特别版本。该模型是在专门的代码数据集上训练的，因此它可以生成代码，且理解提示词中关于代码的自然语言。

Code Llama有四种参数大小，分别是70亿、130亿、340亿和700亿个参数。

所有不同的模型都服务于不同的目的，并且需要的配置也不同。70亿模型可以在单个GPU上运行。相比之下，340亿和700亿模型可以提供更好的结果，但需要更好的配置。

总的来说，如果您的配置不太充足，那么70亿和130亿参数级别的模型是一个不错的选择。

<center>{% button "Code Llama" https://github.com/facebookresearch/codellama %}</center>

## 6. CodeGeeX

![codegeex](https://itsfoss.com/content/images/2024/07/codegeex-1.jpg)

CodeGeeX是最好的GitHub Copilot平替之一，也是同类大模型中数一数二的存在。它是一个代码生成大模型，拥有超过130亿个参数，在超过8500亿个词元上训练。

CodeGeeX具备一些特殊功能，例如跨语言代码翻译，允许您将代码翻译成不同的语言，还免费给Visual Studio Code和其他IDE（集成开发环境）提供可定制的编程助手。可用于所有类型的IDE集成开发环境这一点，使得它成为许多人的完美Copilot替代品。

在Ollama上有一个CodeGeeX这样的AI编程助手，无需再依赖Google搜索查询，只需依靠本地大模型的帮助即可。当然，您可以以此来替代GitHub Copilot。

<center>{% button "CodeGeeX" https://github.com/THUDM/CodeGeeX %}</center>

## 7. Tabby

![tabby AI assistant](https://itsfoss.com/content/images/2024/07/tabby-AI.jpg)

在社区积极开发下，Tabby是GitHub Copilot开源平替中最具特色的一个，可以在众多IDE中作为扩展使用，例如 Visual Code。

在微软Copilot AI的开源自托管替代品中，Tabby可以说是最令人印象深刻。

It can create code snippets from comments and contextual code and unlike some other copilot alternatives, it runs on your infrastructure. Written in Rust, Tabby is designed with performance in mind. You also have a [live demo](https://demo.tabbyml.com/) to test it out before installing it.
Tabby可以从注释和上下文代码中创建代码片段。并且与其他一些copilot的替代品不同，它在您的基础设施上运行。Tabby用Rust编写而成，旨在提高性能。在安装前，还可以通过[在线网站](https://demo.tabbyml.com/)试用。

Customization is straightforward with it. You have a number of open-source LLMs, like StarCoder, CodeLlama, and DeepseekCode, to choose from. You can also provide access to your repository model, so Tabby has more context. It can be a nice AI coding companion.
Tabby是一个很好的AI编程助手，使用它进行自定义非常简单，可以从StarCoder、CodeLlama、DeepseekCode等多个开源大模型中选择。您还可以提供存储库模型的访问权限，以便Tabby有更多上下文。。

<center>{% button "Tabby" https://tabby.tabbyml.com/ %}</center>

## 8. StarCoder

![starcoder](https://itsfoss.com/content/images/2024/07/starcoder-1.jpg)

StarCoder是一款专注于代码的大模型，训练内容包含80多种编程语言、Git commit、GitHub issue和Jupyter notebook，训练参数超过150亿，拥有超过1万亿个词元。

StarCoder模型的可输入文本比其他任何开源大模型都长，上下文长度超过8000个词元。虽然可能不太出名，但是一个不错的AI编程助手。

还有一个名为Starcoder2的版本，包含的数据集是Starcoder的4倍，具备三种参数级别，分别是30亿、70亿和150亿，在3.3到4.3万亿个词元上训练。

<center>{% button "StarCoder" https://huggingface.co/bigcode/starcoder %}</center>

## 9. Deepseek Coder

![deepseek coder](https://itsfoss.com/content/images/2024/07/deepseek-coder-1.jpg)

Deepseek Coder系列提供了从10亿到330亿的模型，从头开始在超过 2 万亿个词元上训练，是一个高性能的编程大模型。与GPT 4等专有大模型相比，性能也十分出色。

由于该模型的原始团队位于中国，该模型同时使用了中文和英文进行训练。

Deepseek Coder的13亿参数版本任务完成速度十分迅速，而330亿版本可以执行最复杂的任务，窗口大小为16K。您可以将它用作最轻量级的copilot替代品之一。

<center>{% button "Deepseek Coder" https://github.com/deepseek-ai/DeepSeek-Coder %}</center>

## 10. DolphinMixtral

![dolphinmixtral](https://itsfoss.com/content/images/2024/07/dolphin-mixtral-1.jpg)

Dolphin模型在Mixtral 8x7B基础上，额外添加了Synthia、OpenHermes、PureDove、New Dolphin-Coder和MagiCoder的数据集，使其比Mixtral更有效率。好吧，这确实是一个有趣的组合。

需要注意的是，这个模型是完全未经审查的。

DolphineMixtral只是Mixtral的一个普通微调版本，没有偏见。您可以根据您的用途调整它。

<center>{% button "DolphinMixtral" https://huggingface.co/cognitivecomputations/dolphin-2.5-mixtral-8x7b %}</center>

即使上文提到了众多AI编程助手，但根据具体的场景，您可以使用任何其他的开源AI聊天机器人。在以下的网址中，我尝试选择出最好的几个聊天机器人，但仍有无数选择待您探索：

{% link https://itsfoss.com/open-source-llms/ 14 Top Open Source LLMs For Research and Commercial Use icon:https://itsfoss.com/content/images/2024/05/open-source-llms.png %}

## 总结

以上提到了很多开源编程大模型，其中一些完全可以作为Copilot的开源平替。所有这些大模型都非常强大，可以帮助您解决几乎所有编程问题。

几乎每个大模型都提供不同的参数版本，以满足各种使用场景。赶快选择一个试试吧！
