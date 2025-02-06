---
title: "LibreChat：集中管理你的 AI 模型"
date: {{release_date}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/librechat-linux.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/librechat-linux.png
categories:
  - 翻译
  - 技术
tags: 
  - AI
authorInfo: |
  via: https://itsfoss.com/librechat-linux

  作者：[Abhishek Kumar](https://itsfoss.com/author/abhishek-kumar/)
  选题：[excniesnied](https://github.com/excniesNIED)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

这是一个开源项目，能够让你通过统一的界面与各种 AI 模型进行交互。下面是我在 Linux 系统上安装它的过程。

<!-- more -->

AI 用户经常面临的一个问题是，需要不断切换聊天界面。

ChatGPT 在很多方面表现出色，但 Perplexity 在网络搜索和回答问题方面更胜一筹。

事实上，如果你对当前 AI 的回答不满意，可能会想向另一个 AI 模型提出相同的问题。

但登录另一个 AI 平台，然后复制粘贴相同的问题，这是一项繁琐的任务。

这就是为什么有些工具允许你通过单一界面使用多个 AI 模型。然而，大多数此类服务都是付费的。

而 [LibreChat](https://www.librechat.ai/) 正是为解决这一问题而生。

让我们深入了解这个改变游戏规则的平台，看看它是如何提升你的数字体验的。

## 什么是 LibreChat AI？

**LibreChat AI** 是一个开源平台，允许用户通过统一的界面与各种 AI 模型进行聊天和交互。你可以使用 OpenAI、Gemini、Anthropic 等其他 AI 模型的 API。你还可以将 [Ollama](https://itsfoss.com/ollama/) 作为端点，使用 LibreChat 与本地大语言模型进行交互。它可以在本地安装，也可以部署在服务器上。

LibreChat 具有高度可定制性，支持广泛的 AI 提供商和服务。下面我来总结一下它的主要特点：

- **免费开源**：所有人都可以免费使用。
- **可定制**：提供丰富的选项，可根据个人喜好定制平台。
- **多 AI 支持**：集成了众多 AI 模型和服务。
- **统一界面**：为与不同 AI 模型交互提供一致的体验。

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-homepage.png 'LibreChat 官方网站首页' %}

## 安装 LibreChat

安装并运行 LibreChat AI 的过程很简单，主要有两种方法：**NPM** 和 **Docker** 安装。

虽然这两种方法各有优势，但 **我更喜欢 Docker 方法，因为它简单高效**。不过，在本文中我们将对两种方法都进行探讨。

你也可以参考 [官方文档](https://www.librechat.ai/docs) 获取 LibreChat 的详细安装说明。不得不说，他们提供了一份全面的指南，涵盖了安装过程的每一个步骤，做得非常出色。

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-documentation.png 'LibreChat 文档页面' %}

### 方法一：使用 NPM 安装 LibreChat

在开始安装之前，请确保你已经具备项目所需的所有先决条件：

**先决条件**：

- Node.js 18+：[https://nodejs.org/en/download](https://nodejs.org/en/download)
- Git：[https://git-scm.com/download/](https://git-scm.com/download/)
- MongoDB（Atlas 或社区服务器）
  - [MongoDB Atlas](https://www.librechat.ai/docs/configuration/mongodb/mongodb_atlas)
  - [MongoDB 社区服务器](https://www.librechat.ai/docs/configuration/mongodb/mongodb_community)

安装完成后，你就可以开始设置你的类 OpenAI 克隆界面了。

**准备安装环境**

首先，你需要克隆官方的 LibreChat 仓库，因为其中包含了构建 LibreChat 所需的所有文件：

```bash
git clone https://github.com/danny-avila/LibreChat.git
```

进入克隆的目录：

```bash
cd LibreChat
```

现在，从 `.env.example` 文件创建一个 `.env` 文件：

```bash
cp.env.example.env
```

{% note color:red 🚧 编辑新创建的 `.env` 文件，将 `MONGO_URI` 更新为你自己的 %}

![img](https://itsfoss.com/content/images/2024/07/librechat-mongodb-uri.png)

**构建 LibreChat**

在完成准备步骤后，我们就可以通过几个简单的步骤从源代码构建项目。

安装依赖项：

```bash
npm ci
```

{% image https://itsfoss.com/content/images/2024/07/librechat-installing-dependencies-1.png '下载所有依赖项' %}

这个命令将构建 LibreChat 的前端：

```bash
npm run frontend
```

{% image https://itsfoss.com/content/images/2024/07/librechat-building-frontend.png '构建 LibreChat 的前端' %}

{% note color:cyan 💡 在文档中，他们直接构建了后端，但在测试过程中，我发现你首先需要运行 MongoDB 服务器。否则会抛出错误，根本无法工作。 %}

MongoDB 需要一个数据目录来存储其数据文件。因此，在你的系统上创建一个目录，用于存储 MongoDB 数据文件（例如，`/path/to/data/directory`）。

之后，你需要进入 MongoDB 安装的目录，即 `/usr/bin`，然后输入以下命令：

```bash
./mongod --dbpath=/path/to/data/directory
```

现在你可以构建后端（忽略错误）：

```bash
npm run backend
```

[![img](https://itsfoss.com/content/images/2024/07/librechat-server-started-at-localhost.png)](https://itsfoss.com/content/images/2024/07/librechat-server-started-at-localhost.png)

你已经成功安装了 LibreChat。你可以通过访问 [http://localhost:3080/](http://localhost:3080/) 来使用它。

### 方法二：使用 Docker 安装 LibreChat

好吧，听我说！这能解释我的无奈。我只用了一行命令就在 Docker 中运行了 LibreChat。在经历了上面的弹窗和依赖错误之后，这简直轻而易举。

**请确保你的系统上已经安装了 Git 和 Docker。**

前几个步骤和克隆仓库一样：

```bash
git clone https://github.com/danny-avila/LibreChat.git
```

并从 `.env.example` 文件创建 `.env` 文件：

```bash
cp.env.example.env
```

我们克隆的仓库中已经提供了 Docker 组合文件，所以我们只需要运行 Docker 即可：

```bash
sudo docker compose up -d
```

{% image https://itsfoss.com/content/images/2024/07/librechat-docker-compose.png 在 Docker 上运行 LibreChat %}

要访问 LibreChat，请访问 [http://localhost:3080/](http://localhost:3080/)。

## 首次运行 LibreChat

开始使用 LibreChat 需要一个简单的登录过程。

[![注册 LibreChat](https://itsfoss.com/content/images/2024/07/librechat-login.png)](https://itsfoss.com/content/images/2024/07/librechat-login.png)

你需要先注册才能登录。

[![在 LibreChat 上创建账户](https://itsfoss.com/content/images/2024/07/librechat-signup.png)](https://itsfoss.com/content/images/2024/07/librechat-signup.png)

完成初始步骤后，你会看到一个简约的界面，几乎让人联想到 ChatGPT 的简洁设计。这种简洁的设计将重点完全放在对话上。

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-homepanel.png LibreChat 初印象 %}

还有一个创建自定义提示的选项：

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-system-prompt.png 为 LibreChat 创建提示面板（点击展开） %}

你可以通过设置面板根据自己的喜好自定义 LibreChat：

[![探索 LibreChat 的设置面板](https://itsfoss.com/content/images/2024/07/librechat-settings.png)](https://itsfoss.com/content/images/2024/07/librechat-settings.png)

对一些人来说，它可能不像其他一些平台那样视觉冲击力强，但这种简洁令人耳目一新，让你可以毫无干扰地直接与 AI 进行交互。

## 使用 API 访问 AI 模型

LibreChat 就像是通往各种 AI 模型的门户。它提供了一个平台，让你可以访问并利用其他提供商的模型功能，如 OpenAI 的 ChatGPT、Google 的 Gemini 等。

这意味着，要充分体验 LibreChat 的潜力，你需要获得这些外部 AI 服务的 API 访问权限。

在本教程中，我使用了 Google 的 Gemini（免费）API 与我们的 AI 助手进行对话。遗憾的是，在测试过程中，OpenAI 标记并封禁了我的账户，所以我无法测试其 API。

### 获取 Google 的 API 密钥：

对于 Google，你可以使用 **生成式语言 API**（用于 Gemini 模型），或者 **Vertex AI API**（用于 Gemini、PaLM2 和 Codey 模型）。

要通过 Google AI Studio 使用 Gemini 模型，你需要一个 API 密钥。如果你还没有，请在 [Google AI Studio](https://aistudio.google.com/app/apikey) 中创建一个密钥。

获得密钥后，将其输入到你的 `.env` 文件中，这样你的实例的所有用户都可以使用它：

```bash
GOOGLE_KEY=mY_SeCreT_w9347w8_kEY
```

或者，你可以通过图形用户界面输入密钥，选择你喜欢的 AI 提供商，在我们的例子中是 Google：

[![在 LibreChat 中添加 Gemini](https://itsfoss.com/content/images/2024/07/librechat-selecting-google-gemini.png)](https://itsfoss.com/content/images/2024/07/librechat-selecting-google-gemini.png)

之后，系统会提示你输入 API 密钥：

[![在 LibreChat 中添加 Gemini](https://itsfoss.com/content/images/2024/07/librechat-gemini-api-gui.png)](https://itsfoss.com/content/images/2024/07/librechat-gemini-api-gui.png)

现在我们可以和我们的聊天机器人聊天了。

## 测试结果

由于 LibreChat 在本质上是对存储在大型数据中心的强大 AI 模型的封装，你可以期待它有极快的响应速度和极低的延迟。

以下是一些测试结果：

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-response-difference-between-arm-x86.png 'LibreChat 对 ARM 和 X86 架构差异问题的回复' %}

另一个例子：

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-response-nextcloud-docker.gif 'LibreChat 对创建 Nextcloud 的 docker-compose 文件问题的回复' %}

根据 [文档](https://www.librechat.ai/blog/2024-03-02_ollama)，LibreChat 还可以与 Ollama 集成。这意味着，如果你 [在系统上安装了 Ollama](https://itsfoss.com/ollama-setup-linux/)，就可以在 LibreChat 中运行本地大语言模型。

也许我们将来会专门写一篇关于集成 LibreChat 和 Ollama 的教程。

## 总结

对于寻求 AI 交互方式的用户来说，LibreChat 是一个很有吸引力的选择。它的开源性质以及利用多个 AI 模型的能力，提供了一定程度的灵活性和潜在的定制性，这是专有平台可能缺乏的。

作为替代方案，对于那些无法使用 Windows 上的 Copilot 的 Linux 用户来说，LibreChat 可能是一个有吸引力的选择。

遗憾的是，由于账户限制，我无法亲自测试 OpenAI API，这一限制阻碍了更全面的评估，特别是「与文档聊天」功能。

尽管如此，LibreChat 的潜力仍然是不可否认的，它的发展值得关注。

如果你还知道其他开源 AI 项目，欢迎与我们分享！