---
title: '使用别名提高你在 Linux 终端中的效率'
date: 
author:
- fosscope-translation-team
- cys2004
- <校对者ID>
banner: https://static.fosscope.com/articles_img/2024/04/linux-alias/alias-command.webp
cover: https://static.fosscope.com/articles_img/2024/04/linux-alias/alias-command.webp
categories:
- 翻译
- 技术
tags:
- Linux
- alias
- tutorial
- tricks
authorInfo: |
  via: https://itsfoss.com/linux-alias/

  作者：[Sagar Sharma](https://itsfoss.com/author/sagar/)
  选题：[cys2004](https://github.com/cys2004)
  译者：[cys2004](https://github.com/cys2004)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出

---

释放终端中别名的超能力吧！

<!-- more -->

通过创建常用命令组合的别名，你可以在 Linux 终端中提高工作效率。

例如，要更新我的 Ubuntu 系统，我不会使用以下命令：

```
sudo apt update && sudo apt upgrade -y
```

而是使用`upd`，效果是一样的。为什么？因为我为上述更新命令组合设置了一个别名`upd`。

```
alias upd="sudo apt update && sudo apt upgrade -y"
```

听起来很神奇，对吧？确实如此。让我们详细讨论一下别名。

## Linux 中的别名命令是什么？

别名命令允许你基于现有的 Linux 命令创建 「自定义命令」。它主要用于为冗长的 Linux 命令组合创建较短形式的缩写。因此，你可以创建一个名为`ftext`的别名来代替`find / -type f -name *.txt`，并使用这个更简洁的命令。

当你经常使用某些命令组合时，这特别有用。你无需根据记忆手动输入这些命令，或是从你的脚本集合中把它们复制下来。你只需要创建一个别名就能快速使用它们。

## 如何在Linux中创建别名？

要为当前会话创建一个别名，可以按照以下方式使用别名命令：

```
alias 别名="你的自定义命令"
```

如果你的命令由多个单词组成，那么引号将是必需的。换句话说，你可以将`gg`设置为`grep`的别名，但是不能将`gg`设置为`grep --color=auto`的别名。它必须是`gg='grep --color=auto'`。

你可以根据需要来使用单引号或双引号。

{% note color:yellow 💡 在使用别名命令时，等号两侧不应该有空格。 %}

让我们举一个简单的例子。

假设你经常使用`ls -la`。在这种情况下，你可以为`ls`命令创建一个别名，当你只输入`ls`时，它会执行`ls -la`。

是的，你可以用同名的别名替代现有命令。

```
alias ls="ls -la"
```

![create-temporary-alias-for-the-ls-command](https://static.fosscope.com/articles_img/2024/04/linux-alias/create-temporary-alias-for-the-ls-command.webp)

如你所见，当我执行`ls`时，它自动执行了`ls -la`。

然而，这个别名只是暂时生效的。如果你退出了终端会话，下次启动终端时先前设置的别名将不再起作用。

### 使别名长期有效

如果你想创建一个长期有效的别名，你需要修改你的`.bashrc`文件。

首先，打开`.bashrc`文件进行编辑：

```
nano ~/.bashrc
```

使用`Alt + /`在 nano 文本编辑器中跳转到文件末尾，并按照以下示例添加行：

```
alias 别名='你的自定义命令'
```

例如，在这里我为`ls -lah`创建了一个别名，当我使用`ls`时将执行`ls -lah`：

```
alias ls='ls -lah'
```

![create-Permanent-alias-for-the-ls-command-in-Linux](https://static.fosscope.com/articles_img/2024/04/linux-alias/create-Permanent-alias-for-the-ls-command-in-Linux.webp)

完成后，保存并退出 nano 文本编辑器。

要使更改生效，需要重新加载`.bashrc`文件：

```
source ~/.bashrc
```

就是这样！

{% note color:yellow 💡 你可以在通过在别名前加上`\`来绕过别名。例如，如果你将`ls`设置为`ls -lah`的别名，你可以输入`\ls`来仅运行`ls`而不是`ls -lah`。 %}

## 如何列出所有别名？

要列出所有已存在的别名，只需执行以下命令：

```
alias
```

![list-existing-alias-in-Linux](https://static.fosscope.com/articles_img/2024/04/linux-alias/list-existing-alias-in-Linux.webp)

如你所见，这里已经为`--color=auto`设置了一个别名，这就是`ls`命令默认使用不同颜色来表示文件、目录和符号链接的原因。

## 你使用别名吗？

相信我，别名非常方便，特别是当你经常在终端中工作时。我知道有些系统管理员会保留一个长长的别名列表，从而避免查找和输入复杂的命令。

那么你呢？你有在 Linux 系统上使用别名吗？又有哪些你为之感到自豪的别名呢？如果它们不涉及敏感信息，欢迎在评论中分享！
