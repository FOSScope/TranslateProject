---
title: Google Introduces Open-Source AI Agent for Developers
date: {{release_date}}
author:
  - fosscope-translation-team
  - excniesNIED
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/google-new-project-oscar.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/google-new-project-oscar.png
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

Google being the good guy for project maintainers.

<!-- more -->

Google, even though it has a reputation of aggressively taking advantage of user data, it also has had a long track record of contributing to [open-source projects](https://opensource.google/projects), and even open-sourcing [theirs](https://news.itsfoss.com/google-open-source-tools-ai/).

Needless to say, the craze surrounding artificial intelligence has not gone unseen by them, and they have been busy coming up with new AI-powered solutions to tackle the ever-evolving digital landscape.

One recent instance has been the introduction of an open-source framework for creating AI-powered helpers, or “*agents*” under **Project Oscar**, for helping with software development and maintenance.

## Project Oscar: Rise Of AI Agents?

```
{% video youtube:986_MUsOk1g %}
```

With an aim to improve open-source software development, Oscar is **an experimental open-source contributor agent architecture** that can be used to deploy agents into a repository for things like handling incoming issues, matching questions with existing documentation, and more.

Some **key goals of this project** include reducing maintainer effort on things like addressing issues, change lists, pull requests, forum questions, and paving the way for more productive maintenance of software.

However, this project is under the wings of the [Go project](https://go.dev/project), and may or may not be made into a separate project in the future. This doesn't mean that it can only be used with Go, the developers want it to be flexible enough for use with other projects as well.

Google says that they have identified **three main capabilities** that will be part of Oscar:

- Taking advantage of natural language to control deterministic tools.
- Indexing/surfacing project related context during contributor interactions.
- Examining any issue reports, change lists and pull requests to try to improve them after submission.

If you are interested in seeing an Oscar agent in action, the Go project uses an Oscar-based agent called [Gaby](https://github.com/gabyhelp) (Go AI Bot), that can be seen in the GitHub repository for Go, handling [issues](https://github.com/golang/go/issues?q=label%3Agabywins&), and posting as *@gabyhelp*.

### Want to check it out?

As mentioned earlier, Oscar is part of the Go project, and those who are interested in checking it out can do so by visiting the [official repo](https://go.googlesource.com/oscar/), where they will also find more information on how it works.

<center>{% button "Oscar" https://go.googlesource.com/oscar/ %}</center>

If you have any doubts, or want to pitch an idea for Oscar, then you can do so on [GitHub](https://github.com/golang/go/discussions/68490).
