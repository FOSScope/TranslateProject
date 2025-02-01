---
title: "Microsoft’s Phi-4 AI Model Goes Open Source!"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
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
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

Microsoft's Phi-4 AI model, one of Azure's exclusive options, is now available for everyone to test!

<!-- more -->

The rise of open source AI models has been a game changer, with many organizations and individuals opting for these models over proprietary ones due to their lower entry costs.

These models also enable fine-tuning for specific use cases, offering unmatched flexibility and fostering collaboration across industries.

[Microsoft](https://www.microsoft.com/) has been a notable player in the space, and following [an announcement](https://x.com/sytelus/status/1877015492126220594) by Shital Shah, an engineer at their research division, they have open-sourced Phi-4, a small language model ([*SLM*](https://www.ibm.com/think/topics/small-language-models)).

## Phi-4 Goes Open: What To Expect?

<img alt="a screenshot of the phi-4 page on hugging face" height="737" width="1560" />\<img src="https://news.itsfoss.com/content/images/2025/01/Phi-4\_HuggingFace\_Page.png" class="kg-image" alt="a screenshot of the phi-4 page on hugging face" loading="lazy" width="1560" height="737" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/Phi-4\_HuggingFace\_Page.png 600w, https://news.itsfoss.com/content/images/size/w1000/2025/01/Phi-4\_HuggingFace\_Page.png 1000w, https://news.itsfoss.com/content/images/2025/01/Phi-4\_HuggingFace\_Page.png 1560w" sizes="(min-width: 720px) 720px"\>Phi-4 on Hugging Face.

Distributed under the [MIT License](https://opensource.org/license/mit), Phi-4 is **a state-of-the-art 14 billion parameter SML** that has been tailored for carrying complex reasoning tasks, outperforming popular models like [Llama 3.3](https://www.llama.com/docs/model-cards-and-prompt-formats/llama3_3/) and [GPT-4o mini](https://openai.com/index/gpt-4o-mini-advancing-cost-efficient-intelligence/) in benchmarks like [MATH](https://arxiv.org/abs/2103.03874) and [GPQA](https://arxiv.org/abs/2311.12022).

Initially exclusive to [Azure AI Foundry](https://ai.azure.com/), Phi-4 is now available to everyone, offering **a powerful utility for tasks requiring complex reasoning and nuanced understanding**. It can be applied in areas like natural language inference, text summarization, content generation, and more.

This flexibility makes Phi-4 suitable for a wide range of applications, including research, product development, and experimentation in AI-powered solutions.

**As for the benchmarks**, here is a table that shows the Phi-4 pitched against other popular models, both small and large. 👇

<img alt="a screenshot that shows a bunch of tables with benchmark numbers pitching the phi-4 model against other models" height="634" width="997" />\<img src="https://news.itsfoss.com/content/images/2025/01/Phi-4\_Benchmarks.png" class="kg-image" alt="a screenshot that shows a bunch of tables with benchmark numbers pitching the phi-4 model against other models" loading="lazy" width="997" height="634" srcset="https://news.itsfoss.com/content/images/size/w600/2025/01/Phi-4\_Benchmarks.png 600w, https://news.itsfoss.com/content/images/2025/01/Phi-4\_Benchmarks.png 997w" sizes="(min-width: 720px) 720px"\>Source: Microsoft Research

If you're looking for a more detailed understanding of Phi-4, be sure to check out the [technical paper](https://arxiv.org/pdf/2412.08905) for an in-depth summary. It provides valuable insights into how the model works and the research behind it.

### Want To Check It Out?

The downloadable weights for Phi-4 can be found on [Hugging Face](https://huggingface.co/microsoft/phi-4), where you will also find the model card. If you are still eager to learn more, then you can go through the initial [announcement blog](https://techcommunity.microsoft.com/blog/aiplatformblog/introducing-phi-4-microsoft%E2%80%99s-newest-small-language-model-specializing-in-comple/4357090).

[Phi-4 (Hugging Face)](https://huggingface.co/microsoft/phi-4)
