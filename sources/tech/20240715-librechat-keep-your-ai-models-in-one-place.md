---
title: LibreChat: Keep Your AI Models in One Place
date: {{release_date}}
author:
  - fosscope-translation-team
  - {{translator}}
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
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: false # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

An open source project that lets you interact with various AI models from one unified interface. Here's how I set it up on my Linux system.

<!-- more -->

One problem AI users often face is the constant need to switch the chat interface.

ChatGPT might be good at many things but Perplexity is better at searching the web and answering your questions.

In fact, you may feel like asking the same question to another AI model if you are not satisfied with the current AI's answer.

But logging into another AI and then copy pasting the same questions is cumbersome task.

This is why there are tools that allow you to use more than one AI model from a single interface. However, most of such services are paid.

And this is where [LibreChat](https://www.librechat.ai/) comes into the picture.

Let's dive in and discover how this game-changing platform can enhance your digital experience.

## What is LibreChat AI?

**LibreChat AI** is an open-source platform that allows users to chat and interact with various AI models through a unified interface. You can use OpenAI, Gemini, Anthropic and other AI models using their API. You may also use [Ollama](https://itsfoss.com/ollama/) as an endpoint and use LibreChat to interact with local LLMs. It can be installed locally or deployed on a server.

LibreChat is designed to be highly customizable and supports a wide range of AI providers and services. Let me summarize its main features:

- **Free and Open Source:** Accessible to everyone without any costs.
- **Customization:** Offers extensive options to tailor the platform to individual preferences.
- **Multi-AI Support:** Integrates with numerous AI models and services.
- **Unified Interface:** Provides a consistent experience for interacting with different AI models.

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-homepage.png LibreChat Official website homepage %}

## Installing LibreChat

Getting LibreChat AI up and running is a straightforward process, with two primary methods: **NPM** and **Docker** installation.

While both options offer advantages, **Docker is my preferred choice for its simplicity and efficiency**. However, we'll explore both in this article.

You can also refer to the [official documentation](https://www.librechat.ai/docs) for detailed installation instructions on LibreChat. I must say that they have done a great job by providing a comprehensive guide covering every step of the process.

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-documentation.png LibreChat documentation page %}

### Method 1: Install LibreChat with NPM

Before you begin with the installation, make sure that you have all the prerequisites for our project:

**Prerequisites:**

- Node.js 18+: [https://nodejs.org/en/download](https://nodejs.org/en/download)
- Git: [https://git-scm.com/download/](https://git-scm.com/download/)
- MongoDB (Atlas or Community Server)
  - [MongoDB Atlas](https://www.librechat.ai/docs/configuration/mongodb/mongodb_atlas)
  - [MongoDB Community Server](https://www.librechat.ai/docs/configuration/mongodb/mongodb_community)

Once they are installed, you can move forward setting-up your openAI clone interface.

**Preparing installation environment**

First, you need to clone the official LibreChat repository as it contains all the files you need to build LibreChat:

```bash
git clone https://github.com/danny-avila/LibreChat.git
```

Navigate to the cloned directory:

```bash
cd LibreChat
```

Now you create a `.env` file from the `.env.example`

```bash
cp .env.example .env
```

{% note color:red 🚧 Edit the newly created `.env` file to update the `MONGO_URI` with your own %}

![img](https://itsfoss.com/content/images/2024/07/librechat-mongodb-uri.png)

**Building LibreChat**

Once the preparation steps have finished, we can build the project from the source in a few simple steps.

To install the dependencies:

```bash
npm ci
```

{% image https://itsfoss.com/content/images/2024/07/librechat-installing-dependencies-1.png Downloading all the dependencies %}

This command will build the frontend of LibreChat:

```bash
npm run frontend
```

{% image https://itsfoss.com/content/images/2024/07/librechat-building-frontend.png Building the frontend of LibreChat %}

{% note color:cyan 💡 In the documentation, they directly build the backend, but during testing, I learned that you first need to run the MongoDB server. Otherwise, it'll throw errors and won't work at all. %}

MongoDB requires a data directory to store its data files. Thus, create a directory on your system where you want to store the MongoDB data files (e.g., `/path/to/data/directory`).

After that, you need to be in the same directory where the MongoDB has been installed i.e. `/usr/bin` then just type this command:

```bash
./mongod --dbpath=/path/to/data/directory
```

Now you can build the backend (ignore the errors):

```bash
npm run backend
```

[![img](https://itsfoss.com/content/images/2024/07/librechat-server-started-at-localhost.png)](https://itsfoss.com/content/images/2024/07/librechat-server-started-at-localhost.png)

You have successfully installed LibreChat. You can access it by visitng [http://localhost:3080/](http://localhost:3080/)

### Method 2: Install LibreChat using Docker

Okay hear me out! This explains my frustration. So, it took me just a one liner command to run LibreChat in Docker. After battling with all the pop-ups & dependency errors, this was like a walk in the park.

**Please ensure that you have Git and Docker installed on your system.**

The first few steps will remain the same like cloning the repository:

```bash
git clone https://github.com/danny-avila/LibreChat.git
```

and creating `.env` file from `.env.example` :

```bash
cp .env.example .env
```

The docker compose file is already provided in the repository that we cloned, thus all we need to do is run our docker:

```bash
sudo docker compose up -d
```

{% image https://itsfoss.com/content/images/2024/07/librechat-docker-compose.png Running LibreChat on Docker %}

To access the LibreChat, visit [http://localhost:3080/](http://localhost:3080/).

## First run of LibreChat

Getting started with LibreChat involves a straightforward login process.

[![Sign up for LibreChat](https://itsfoss.com/content/images/2024/07/librechat-login.png)](https://itsfoss.com/content/images/2024/07/librechat-login.png)

You do have to signup first to login.

[![Creating account on LibreChat](https://itsfoss.com/content/images/2024/07/librechat-signup.png)](https://itsfoss.com/content/images/2024/07/librechat-signup.png)



Once you've navigated that initial step, you're greeted by a minimalist interface that's almost reminiscent of ChatGPT's clean design. It's a no-frills approach that puts the focus squarely on the conversation.

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-homepanel.png LibreChat first look %}

There is an option to create custom prompts as well:

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-system-prompt.png Creating prompt pane for LibreChat (click to expand) %}

You can customize LibreChat to your liking by going to the settings pane:

[![Exploring the settings pane in LibreChat](https://itsfoss.com/content/images/2024/07/librechat-settings.png)](https://itsfoss.com/content/images/2024/07/librechat-settings.png)

While to some people, it might not be as visually striking as some other platforms, the simplicity is refreshing and allows you to dive right into interacting with the AI without distractions.

## Accessing AI models using their API

LibreChat operates as a gateway to various AI models. It provides a platform to access and utilize the capabilities of models from other providers like OpenAI's ChatGPT, Google's Gemini, and others.

This means that to fully experience LibreChat's potential, you'll need to have API access to these external AI services.

For this tutorial, I have used Google's Gemini (free) API to have a conversation with our AI assistant. Unfortunately, I couldn't test with OpenAI's API since during testing they flagged my account and banned me.

### Getting Google's API key:

For Google, you can either use the **Generative Language API** (for Gemini models), or the **Vertex AI API** (for Gemini, PaLM2 & Codey models).

To use Gemini models through Google AI Studio, you’ll need an API key. If you don’t already have one, create a key in [Google AI Studio](https://aistudio.google.com/app/apikey).

Once you have your key, provide the key in your .`env` file, which allows all users of your instance to use it:

```bash
GOOGLE_KEY=mY_SeCreT_w9347w8_kEY
```

Or you can enter it via GUI by selecting your prefered AI provider i.e. Google in our case:

[![Adding Gemini in LibreChat](https://itsfoss.com/content/images/2024/07/librechat-selecting-google-gemini.png)](https://itsfoss.com/content/images/2024/07/librechat-selecting-google-gemini.png)

After that, it'll prompt you to enter your API key:

[![Adding Gemini in LibreChat](https://itsfoss.com/content/images/2024/07/librechat-gemini-api-gui.png)](https://itsfoss.com/content/images/2024/07/librechat-gemini-api-gui.png)

Now we are ready to chat with our Chat BOT.

## Results

Since LibreChat is essentially a wrapper for powerful AI models housed in massive data centers, you can expect lightning-fast response times and minimal latency.

Here are a few results:

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-response-difference-between-arm-x86.png LibreChat's reply to the question about difference between ARM & X86 architecture %}

Another one:

{% image https://itsfoss.com/content/images/size/w1000/2024/07/librechat-response-nextcloud-docker.gif LibreChat's reply to create a docker-compose file for Nextcloud %}

As per [documentation](https://www.librechat.ai/blog/2024-03-02_ollama), LibreChat can also integrate with Ollama. This means that if [you have Ollama installed on your system](https://itsfoss.com/ollama-setup-linux/), you can run local LLMs in LibreChat.

Perhaps we'll have a dedicated tutorial on integrating LibreChat and Ollama in the future.

## Final Thoughts

LibreChat presents an intriguing proposition for users seeking AI interaction. Its open-source nature and ability to leverage multiple AI models offer a degree of flexibility and potential customization that proprietary platforms might lack.

In terms of alternatives, LibreChat could be a compelling option for Linux users who might find Copilot for Windows to be exclusive.

Unfortunately, due to account restrictions, I couldn't personally test the OpenAI API, a limitation that prevented a more comprehensive evaluation, specially the "Chat with documents" feature.

Nevertheless, LibreChat's potential is undeniable, and its evolution will be interesting to watch.

If you have more open source AI projects in mind, feel free to share with us!
