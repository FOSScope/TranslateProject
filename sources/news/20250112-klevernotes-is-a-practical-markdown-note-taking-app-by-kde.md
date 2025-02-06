---
title: "KleverNotes Is A Practical Markdown Note-Taking App By KDE"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - news
tags:
  - Markdown
  - 笔记
  - KleverNotes
authorInfo: |
  via: https://news.itsfoss.com/klevernotes/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

这是一款聪明的 Markdown 编辑器。快来试试吧！

<!-- more -->

📜  
必知亮点 👇  
- 聪明的命名
- 易于上手
- 极简的编辑体验

[Markdown](https://en.wikipedia.org/wiki/Markdown) 作为流行的笔记标记语言，因其简洁性和多功能性备受青睐。其纯文本格式确保了用户无需复杂工具即可快速创建整洁易读的笔记。

多年来涌现出了众多 [Markdown 笔记编辑器](https://itsfoss.com/best-markdown-editors-linux/)，它们都在功能与简洁间寻求平衡。

在本次应用推荐中，我们将聚焦这一领域的新秀 —— **KleverNotes**。

## KleverNotes：Markdown 的正确打开方式

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_a.webp '' %}

该应用的诞生源于首席开发者 [Louis Schul](https://invent.kde.org/louis-schul) 的个人需求：学习 QML 和 C++ 并激励自己在课堂上做笔记。KleverNotes 的首个稳定版本发布于 [2024 年 10 月](https://blogs.kde.org/2024/06/05/klevernotes-version-1-0-official-release/)。

### ⭐ 核心功能

除了"Klever"这个有趣的名称，该应用还**支持通过插件扩展基础 Markdown 功能**，包含语法高亮、快速表情输入、笔记链接和 PlantUML（*用于图表制作*）等实用工具。

核心要素包括：
* **实时预览笔记内容**
* **专为 KDE 生态系统打造**
* **存储格式符合** [**CommonMark**](https://commonmark.org/) **规范**

### 💻 用户体验

笔者在 Fedora 40 笔记本上通过 Flatpak 包体验了 KleverNotes 1.1.0 的笔记工作流。

初次启动时需要**选择笔记存储位置**，通过"*创建存储*"选项可以新建文件夹，也支持选择现有目录。

设置完成后，系统会自动加载演示笔记，其中展示了各类 Markdown 元素的使用技巧。

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_b.webp '' %}

在完成上述配置后，**一个演示笔记会被自动加载，其中展示了 KleverNotes 的各项功能**，并包含对多种 Markdown 元素的说明。通过右键现有分类可轻松创建新类别，并添加多个笔记。

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_c-1.webp '' %}

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_d.webp '' %}

**Markdown 编辑体验令人愉悦**，虽偶有小瑕疵，但整体流畅自然。用户既可直接键入 Markdown 代码，也可通过顶部工具栏的便捷按钮操作（适合笔者这样的懒人）。

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_e.webp '' %} 

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_f.webp '' %}

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_g.webp '以编辑 [Bond Forger](https://spy-x-family.fandom.com/wiki/Bond_Forger) 日记为例展示 KleverNotes 的编辑体验。' %}

还可以通过点击工具栏中的图片按钮 **为笔记添加图片**，KleverNotes 会将图片添加到光标所在的行。我既可以从网站添加网络图片，也可以上传本地图片，还能绘制图片。

如果我愿意，我可以让应用程序将上传的图片保存在与笔记相同的文件夹中，以防止图片丢失。我建议你启用此功能，这样你就不会丢失任何重要图片了。 

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_h.webp 'KleverNotes 中的 Markdown 速查表' %}

编辑器左下方提供**Markdown 速查表**，便于用户随时查阅语法元素。

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_i.webp '' %}

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_j.webp '' %}

KleverNotes 也可用于创建待办事项。

在所有笔记旁边，有一个单独的「*TODO*」部分，你可以 **为重要任务创建待办事项**，并在完成后将其勾选。你可以为这些待办事项添加有用的描述，以便轻松跟踪。

如果你注意到上面的截图，**工具栏中的许多按钮是不可见的**。我不得不慢慢将鼠标悬停在它们上面，才能分辨出每个按钮的功能。不过，我使用了快速表情符号插件来装饰任务列表，效果还不错。 

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_l.webp '' %}

{% image https://static.fosscope.com/articles_img/2025/01/KleverNotes_k.webp '插件管理与笔记预览设置界面' %}

但要首先启用该功能，用户必须进入「插件」设置页面并手动开启。同样，设置菜单中还包含其他一些实用选项，可用于更改样式、字体和文本颜色。

综上所述，**我真的很喜欢 KleverNotes 所提供的功能**，不过也有一些我期望具备的功能，比如界面的暗黑模式，以及便捷的笔记导入/导出方式。

然而，考虑到这款应用相对较新，这些不足也是可以理解的。由于它隶属于 KDE 旗下，未来很可能会定期获得更新和改进。 

## ⚙️ Linux 安装指南

目前可通过 [Flathub](https://flathub.org/apps/org.kde.klevernotes) 获取，源码托管于 [GitLab](https://invent.kde.org/office/klevernotes)。遇到问题可加入其 [Matrix 频道](https://matrix.to/)交流。

[KleverNotes (Flathub)](https://flathub.org/apps/org.kde.klevernotes)