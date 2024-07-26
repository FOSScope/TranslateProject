---
title: GitHub Copilot Alternatives: Best Open Source LLMs for Coding
date: {{release_date}}
author:
  - fosscope-translation-team
  - {{translator}}
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
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Looking to deploy an AI model for coding or just want an open-source GitHub Copilot replacement? We got you!

<!-- more -->

AI is everywhere. One of the most important types of AI models is Large Language Models (LLMs).

Of course, we are talking about the [open-source LLMs](https://itsfoss.com/open-source-llms/) (not the proprietary ones). While these LLMs help a great deal with generating text, helping you brainstorm with ideas, unleashing your creativity with images, they are also capable of helping you in the coding process. So, you can write code faster.

For that, you need LLMs that are fine-tuned and trained with programming languages for you to get results geared towards coding.

Here, I shall mention some useful open-source LLMs for coding, along with a couple of open GitHub Copilot alternatives.

{% note color:cyan 📋 You can find all the open source LLMs on Ollama and get it installed locally without much hassle. %}

## 1. WizardCoder

![wizardcoder](https://itsfoss.com/content/images/2024/07/wizardcoder-huggingface-1.jpg)

[WizardCoder](https://github.com/nlpxucan/WizardLM) is an open-source code Large Language Model (LLM) optimized on Llama 2. It can handle complex instructions well and has been fine-tuned accordingly.

The Evol-Instruct algorithm used ensures that the model is fine-tuned with more complete and rich instructions, making the WizardCoder model shine for coding tasks. The model claims that it outperforms Gemini Pro, ChatGPT 3.5, and more, thanks to this algorithm. So, a pretty good LLM for an AI coding assistant.

The latest release at the time, **WizardCoder-33B-V1.1** is trained from deepseek-coder-33b-base. You can also use their variants like WizardCoder-Python-34B-V1.0.

It is available in the [Ollama](https://itsfoss.com/ollama/) library if you want to try it out.

<center>{% button "WizardCoder" https://huggingface.co/WizardLMTeam/WizardCoder-15B-V1.0 %}</center>

**Suggested Read 📖**

{% link https://itsfoss.com/ollama-setup-linux/ Running AI Locally Using Ollama on Ubuntu Linux icon:https://itsfoss.com/content/images/2024/05/run-ai-locally-in-linux-using-ollama.png %}

## 2. Phind CodeLlama

![phind codellama](https://itsfoss.com/content/images/2024/07/phind-code-model-1.jpg)

Phind is one of the [best AI search engines](https://itsfoss.com/ai-search-engines/), but their code LLM is just as good. Phind CodeLlama is a code generation model based on CodeLlama 34B fine-tuned for instruct use cases.

The model is trained on a dataset that includes high-quality programming problems and solutions. It was also trained using DeepSpeed ZeRO 3 and Flash Attention 2 in three hours on 32 A100-80 GB GPUs.

To guarantee the accuracy of their findings, Phind utilized OpenAI's decontamination technique on their dataset by extracting portions of text from each assessment case and verifying if there were corresponding matches in the trained examples.

Two variations of the model exist: v1 and v2. v1 is built on CodeLlama 34B and CodeLlama-Python 34B. The v2 variant is just an iteration of v1, trained on an additional 1.5B tokens of high-quality programming-related data.

<center>{% button "Phind CodeLlama" https://huggingface.co/Phind/Phind-CodeLlama-34B-v2 %}</center>

## 3. Mistral7B and Mixtral-8x7B

![mistral AI](https://itsfoss.com/content/images/2024/07/mistral-ai-1.jpg)

Developed by Mistral AI, both Mistral7B and Mixtral 8x7B hail themselves as the best models of their respective sizes. Mistral 7B has a 7.3B parameter and outperforms Llama 2 13B on benchmarks.

I did find it running faster when using Ollama on my Ubuntu system.

Some technical details: greater in size, Mixtral 8x7B is a Sparse Mixture-of-Experts (SMoE) model with 46.7B parameters. Although it has a large number of parameters, it only requires 12.9B parameters for each token.

Both models can be fine-tuned according to the task you need to accomplish. However, it also works for coding.

<center>{% button "Phind CodeLlama" https://huggingface.co/Phind/Phind-CodeLlama-34B-v2 %}</center>

## 4. CodeBooga

![codebooga](https://itsfoss.com/content/images/2024/07/codebooga-1.jpg)

Codebooga is a superb open-source code LLM, mainly because it is a merge of Phind-Codellama 34B v2 and WizardCoder-Python-34B-V1.0. It seems it is one of the best models to use for Python and JavaScript coding tasks.

It features 33.4 billion parameters in total and could be better than the models merged when you evaluate it for your use-case.

CodeBooga may not be as popular, but it is also available in the Ollama library for you to try.

<center>{% button "CodeBooga" https://huggingface.co/oobabooga/CodeBooga-34B-v0.1 %}</center>

## **5. Code Llama**

![codellama](https://itsfoss.com/content/images/2024/07/codellama-1.jpg)

Developed by Meta AI, [Code Llama](https://github.com/facebookresearch/codellama) is a specialized version of Llama 2. This model is trained on a code-specific dataset; hence, it can generate code and understand natural language about code from any prompts.

There are four sizes of Code Llama, namely 7B, 13B, 34B, and 70B parameters respectively.

All the different models serve different purposes and require various levels of resources. The 7B model can run on a single GPU. Comparatively, the 34B and 70B offer better results, requiring more resources.

Overall, if you do not have much resources to spare, the 7B and 13B models can be a good pick.

<center>{% button "Code Llama" https://github.com/facebookresearch/codellama %}</center>

## 6. CodeGeeX

![codegeex](https://itsfoss.com/content/images/2024/07/codegeex-1.jpg)

CodeGeeX is one of the best GitHub Copilot alternatives, the first of its type on the list. It is a code-generation LLM with over 13 billion parameters, trained on more than 850 billion tokens.

CodeGeeX offers some special features, such as Crosslingual Code Translation which allows you to translate code into different languages. It is also available for Visual Studio Code and other IDEs (Integrated Development Environment) for free as a customizable programming assistant. The integrations available for all kinds of IDEs make it a perfect Copilot alternative for many.

With AI coding assistants like this on top of Ollama, you don't have to rely on Google search queries, but just the LLM to help you out locally. Of course, you can replace GitHub Copilot with these solutions.

<center>{% button "CodeGeeX" https://github.com/THUDM/CodeGeeX %}</center>

## 7. Tabby

![tabby AI assistant](https://itsfoss.com/content/images/2024/07/tabby-AI.jpg)

Tabby is one of the most feature-rich open-source GitHub Copilot alternatives actively being developed by the community. It can be used through many IDEs as an extension, such as Visual Code.

One of the most impressive open-source self-hosted replacement to Microsoft's Copilot AI.

It can create code snippets from comments and contextual code and unlike some other copilot alternatives, it runs on your infrastructure. Written in Rust, Tabby is designed with performance in mind. You also have a [live demo](https://demo.tabbyml.com/) to test it out before installing it.

Customization is straightforward with it. You have a number of open-source LLMs, like StarCoder, CodeLlama, and DeepseekCode, to choose from. You can also provide access to your repository model, so Tabby has more context. It can be a nice AI coding companion.

<center>{% button "Tabby" https://tabby.tabbyml.com/ %}</center>

## 8. StarCoder

![starcoder](https://itsfoss.com/content/images/2024/07/starcoder-1.jpg)

StarCoder is a code-focused LLM trained in over 80 programming languages, Git commits, GitHub issues, and Jupyter notebooks. It is trained on over 15 billion parameters with over 1 trillion tokens.

The StarCoder models can analyze more input than any other open LLM, with a context length of over 8,000 tokens. While it may not be a popular option, it can be a good fit for an AI coding assistant.

There also exists another version called Starcoder2 which consists of a dataset 4 times that of Starcoder. It also comes in three sizes, 3B, 7B, and 15B trained on 3.3 to 4.3 trillion tokens.

<center>{% button "StarCoder" https://huggingface.co/bigcode/starcoder %}</center>

## 9. Deepseek Coder

![deepseek coder](https://itsfoss.com/content/images/2024/07/deepseek-coder-1.jpg)

The Deepseek coder series offers models of size 1B all the way to 33B. Trained from scratch on over 2T tokens, it is a high-performance code LLM. It also showed exceptional performance when compared to proprietary LLMs such as GPT 4.

Considering the origin team for the model is based in China, it has also been trained with Chinese language along with English.

Deepseek coder's 1.3B version offers lightning-fast task completion, while its 33B version can do the most complex of tasks with a 16K window size. You can utilize it as one of the most lightweight copilot alternatives.

<center>{% button "Deepseek Coder" https://github.com/deepseek-ai/DeepSeek-Coder %}</center>

## 10. DolphinMixtral

![dolphinmixtral](https://itsfoss.com/content/images/2024/07/dolphin-mixtral-1.jpg)

The Dolphin Model is based on Mixtral 8x7B with additional datasets of Synthia, OpenHermes, PureDove, New Dolphin-Coder, and MagiCoder, making it a tab bit more efficient than Mixtral. Well, that's an interesting mixture indeed.

A point to note is the fact that this model is completely uncensored.

DolphineMixtral is just a more fine-tuned version of the normal Mixtral without bias. You can tweak it for your use-case.

<center>{% button "DolphinMixtral" https://huggingface.co/cognitivecomputations/dolphin-2.5-mixtral-8x7b %}</center>

Even with all the AI coding companions mentioned, you can utilize any open-source AI-powered chatbot as per your use-cases. I try to pick some of the best, but you have an endless list of choices that you can explore. Some of them can be found here:

{% link https://itsfoss.com/open-source-llms/ 14 Top Open Source LLMs For Research and Commercial Use icon:https://itsfoss.com/content/images/2024/05/open-source-llms.png %}

## Wrapping Up

There are many open LLMs for coding, and some of them tailored to be utilized as open-source alternatives to Copilot. All of these LLMs are extremely capable and help you with almost all of your programming problems.

Almost every LLM here delivers different-sized models for all kinds of usage. So, make your pick and get started!
