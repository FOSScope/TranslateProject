---
title: 微软 Phi-4 AI 模型正式开源！
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2025/01/microsofts-phi-4-ai-model-goes-open-source/ms-phi-4-opensource.webp
cover: https://static.fosscope.com/articles_img/2025/01/microsofts-phi-4-ai-model-goes-open-source/ms-phi-4-opensource.webp
categories:
  - 翻译
  - 新闻
tags:
  - LLM
authorInfo: |
  via: https://news.itsfoss.com/microsofts-phi-4-ai-model-open-source/

  作者：[{{author}}]({{author_link}})
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[Churnie HXCN](https://github.com/excniesnied)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

微软 Azure 平台的独家 AI 模型 Phi-4 现已向公众开放测试！

<!-- more -->

开源 AI 模型的崛起正在改变游戏规则，由于其较低的入门成本，越来越多的机构和个人选择这些模型而非闭源方案。

这些模型还支持针对特定用例进行微调，提供无与伦比的灵活性，并促进跨行业协作。

[微软](https://www.microsoft.com/) 一直是该领域的重要参与者，其研究院工程师 Shital Shah [宣布消息](https://x.com/sytelus/status/1877015492126220594) 后，正式开源了小型语言模型 Phi-4（[*SLM*](https://www.ibm.com/think/topics/small-language-models)）。


## Phi-4 开源意味着什么？

{% image https://static.fosscope.com/articles_img/2025/01/microsofts-phi-4-ai-model-goes-open-source/Phi-4_HuggingFace_Page.webp Hugging Face 平台上的 Phi-4 %}

基于 [MIT许可证](https://opensource.org/license/mit) 发布的 Phi-4 是**拥有 140 亿参数的最先进 SML**，专为复杂推理任务打造，在 [MATH](https://arxiv.org/abs/2103.03874) 和 [GPQA](https://arxiv.org/abs/2311.12022) 等基准测试中表现超越 [Llama 3.3](https://www.llama.com/docs/model-cards-and-prompt-formats/llama3_3/) 和 [GPT-4o mini](https://openai.com/index/gpt-4o-mini-advancing-cost-efficient-intelligence/) 等热门模型。

Phi-4 最初为 [Azure AI Foundry](https://ai.azure.com/) 所独有，现在已向所有人开放，为需要复杂推理和细微理解的任务提供**强大的工具**。它可应用于自然语言推理、文本摘要、内容生成等领域。

这种灵活性使 Phi-4 适用于研究、产品开发、AI 解决方案实验等广泛场景。

**至于基准测试**，下面的表格显示了 Phi-4 与其他流行的小型和大型模型的对比情况。👇

{% image https://static.fosscope.com/articles_img/2025/01/microsofts-phi-4-ai-model-goes-open-source/Phi-4_Benchmarks.webp  来源：微软研究院 %}

如需深入了解 Phi-4 的技术细节，可查阅其 [技术论文](https://arxiv.org/pdf/2412.08905)，获取模型工作原理和研究背景的深度解析。

### 如何获取？

Phi-4 的模型权重文件已发布于 [Hugging Face](https://huggingface.co/microsoft/phi-4)，包含完整的模型文档。更多详细信息可参考微软的 [官方发布博客](https://techcommunity.microsoft.com/blog/aiplatformblog/introducing-phi-4-microsoft%E2%80%99s-newest-small-language-model-specializing-in-comple/4357090)。

<center>{% button "Phi-4 (Hugging Face)" https://huggingface.co/microsoft/phi-4 %}</center>