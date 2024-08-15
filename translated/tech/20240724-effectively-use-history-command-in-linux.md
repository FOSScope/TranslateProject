---
title: 在Linux中有效使用历史命令
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - 2024zht
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/effectly-use-history-commands-linux.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/effectly-use-history-commands-linux.png
categories:
  - 翻译
  - 技术
tags: 
  - Linux命令
authorInfo: |
  via: https://itsfoss.com/history-command/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[2024zht](https://github.com/2024zht)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

在本教程中，掌握 history 命令并学习一些 bash 历史记录功能的有趣用法。

<!-- more -->

随着您越来越多地使用终端，您将不断运行各种命令。

然后你会发现，有时候你需要知道之前运行了哪些命令，或者想要再次运行某个特定的命令。

这就是 Linux 中存在 `history` 命令的原因。它是 shell 的内置命令，对于经常使用终端的人来说极为有用。

由于它是 shell 内置命令，它的行为可能会根据您使用的 shell（如 bash、zsh、ksh 等）以及配置方式略有不同。尽管如此，其核心的基本功能保持不变。

在本教程中，我将介绍 `history` 命令的基本用法，然后展示一些你应该想要了解的有用技巧。

## 检查命令历史记录

你可以反复按上方向键来浏览命令历史记录，但每次只显示一条命令。而 `history` 命令则允许你一次性查看所有之前运行过的命令。

打开终端并运行以下命令：

```
history
```

它显示了你过去运行过的命令。对我来说，它显示了以下内容：

![History command example](https://itsfoss.com/content/images/2024/07/history-command-examples.png)

历史记录通常存储在 `~/.bash_history` 文件中。`~` 表示主目录，以防你不知道。

如果您有所疑问，可以检查 `HISTFILE` 变量来获取您的 shell 的历史文件位置。

```
echo $HISTFILE
```

**历史中存储了多少条命令**？这取决于 `HISTFILESIZE` 变量。在 Debian 和 Ubuntu 系统中，它通常被设置为 2000。

```
echo $HISTFILESIZE
```

{% note color:green 💡 历史记录中的行数太多，让您的屏幕显得杂乱无章？您可以使用 `history N` 命令来选择只显示历史记录的最后 N 行。  %}

## 从历史记录中运行命令

你注意到历史命令在每个命令条目前面显示一个编号了吗？你可以使用这个编号从历史记录中运行命令。例如，要运行历史记录中的第 N 个条目，可以使用：

```
!N
```

这里有一个实际的例子，我运行了历史记录中第152 条命令。

![show only last few lines of the history](https://itsfoss.com/content/images/2024/07/run-command-from-history.png)

## 从最后一次运行的命令中获取更多信息

这并不是 `history` 命令的直接示例，但它涉及命令历史记录，我想讨论它。

你可以使用 `!!` 来获取最后一个运行的命令。当你忘记使用 sudo 运行命令时，这非常有用。你不需要重新输入整个命令，只需使用：

```
sudo !!
```

它将显示正在运行的完整命令。以下是一个例子：

![history trick with sudo command](https://itsfoss.com/content/images/2024/07/history-trick-with-sudo.png)

如果您在之前的命令中出现了任何拼写错误，您可以以下面这种方式来修复它：

```
^foo^bar
```

这将会使得最后一个运行命令中的第一个 `foo` 替换为 `bar`。

这是一个实际的例子：

![fix typo in the last ran command](https://itsfoss.com/content/images/2024/07/fix-typo--in-command-history.png)

{% note color:green 💡 另一个小技巧，这是一个终端快捷键，虽然不是在所有地方都适用，但仍然非常方便。要使用上一个命令的最后一个参数，可以使用 `Alt+.` 键。例如，使用 `ls` 命令查看一个深度嵌套的目录，并且想要切换到该目录中？不需要重新输入所有内容，只需使用 `cd` 命令并按下 `Alt+.` 键即可。  %}

## 在命令历史中搜索

您可以按向上（和向下）键循环浏览命令历史，当您想要的命令出现时按回车键。这对于最近的几个命令来说效果很好，但您不应该为了从历史记录中获取命令而连续按向上键100 次。

![img](https://itsfoss.com/content/images/2024/07/linux-history-command-meme.png)

一种在历史记录中搜索的方法是使用 `grep` 命令进行过滤。

假设你想查找之前运行过的 `tail` 命令：

```
history | grep tail
```

**另一种方法是使用反向搜索功能**。按下 Ctrl+R，您将进入反向搜索界面。开始输入您的搜索词，它将开始显示历史记录中匹配的命令。![Reverse search Linux command history](https://itsfoss.com/content/images/2024/07/reverse-search-command-history.png)

当然，同一个搜索字符串可能会有多个匹配项。反复按 `Ctrl+R` 键可以循环浏览所有匹配项。每次只显示一个匹配项。

如果你找到了你要找的命令，按右箭头键退出反向搜索并开始使用该命令。

按 `Ctrl+C` 退出反向搜索，且不获取任何要使用的命令。

## 从历史记录中删除命令

要从历史记录中删除一个命令，可以使用它在历史记录中的条目编号，方法如下：

```
history -d N
```

在下面的例子中，我删除了编号为 181 的 `flatpak add` 长命令：

![Deleting command from history](https://itsfoss.com/content/images/2024/07/delete-command-history.png)

您也可以提供一个范围来删除多行命令：

```
history -d 160-180
```

{% note color:green 💡 `history -c` 命令将清除整个 Bash 历史记录。  %}

## 从历史记录中排除某些命令

如果您不希望某个命令被记录在历史记录中，只需在该命令前加一个空格并运行即可：

在下面的示例中，我运行了一个不存在的随机命令，但我在它前面加了一个空格。显然，它抛出了一个错误，但没有被记录在历史记录中。

![img](https://itsfoss.com/content/images/2024/07/exclude-command-from-history.png)

您是否注意到第二个 `history 7` 也没有被记录在历史记录中？这是因为 `HISTCONTROL` 环境变量的设置。它可以有以下值：

- ignorespace：在命令前加一个空格来运行它，这样它就不会被包含在历史记录中。
- ignoredups：如果有两个或更多连续运行的相同命令，只有第一个会被记录。
- ignoreboth：同时使用上述提到的两个功能。

{% note color:green 💡 你还可以在 bashrc 文件中设置 HISTIGNORE 变量，并从历史记录中排除一些常见命令。使用方法如下：`HISTIGNORE='pwd:echo *:clear'`  %}

## 额外提示：为什么有些命令没有被记录在历史记录中？

您是否注意到并非所有运行的命令都被记录在历史记录中？如果您同时运行多个终端会话，这可能是原因之一。

确实如此。历史文件 `~/.bash_history` 通常不会在您运行命令后立即更新，而是在您关闭终端会话时才会被修改。

如果您检查 `history` 命令和 `~/.bash_history` 文件的内容，您会发现当前会话中运行的命令并没有出现在 `~/.bash_history` 文件中。

如果您曾经打开过多个终端和标签页，您可能会意识到在一个标签页中最近运行的命令在另一个标签页中按箭头键时是不可用的。这是因为当前会话的命令历史尚未保存到 `~/.bash_history` 文件中。

现在，当您开始关闭终端会话时，只有最后一个关闭的会话的历史记录会被记录下来。其他会话的命令历史则会丢失。这是默认行为。

您可以通过在 `bashrc` 文件中使用 `export PROMPT_COMMAND='history -a'`（追加模式）来改变这一行为。这样做会在显示命令提示符（终端上的那个 $ 符号）之前，将刚刚运行的命令添加到历史文件中。

有些人使用 `export PROMPT_COMMAND='history -a; history -r'`，这不仅记录每个会话的历史，还从其他终端会话中获取命令历史，以便您可以使用向上箭头键来访问它们。这听起来不错，但很快就会变得混乱。是否采用这种做法完全取决于您。

## 总结

即使不直接输入 `history` 命令，我也会经常使用反向搜索和向上箭头键来查找历史命令。但了解历史机制提供的各种功能仍然很有好处。

希望您在本教程中学到了一些关于 `history` 命令的新知识和有趣内容。
