---
title: '使用 Tailspin 带高亮地查看日志文件'
date: 
author:
  - fosscope-translation-team
  - cys2004
  - <校对者ID>
banner: https://static.fosscope.com/articles_img/2024/03/tailspin/logspin-a-logfile-highlighter.webp
cover: https://static.fosscope.com/articles_img/2024/03/tailspin/logspin-a-logfile-highlighter.webp
categories:
  - 翻译
  - 技术
tags:
  - tutorial
  - Tailspin
  - CLI tool
  - Rust
authorInfo: |
  via: https://itsfoss.com/tailspin/

  作者：[Sagar Sharma](https://itsfoss.com/author/sagar/)
  选题：[cys2004](https://github.com/cys2004)
  译者：[cys2004](https://github.com/cys2004)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---
使用 Tailspin 命令行工具，让阅读日志文件变得更加容易和有趣。

<!-- more -->

[阅读日志](https://linuxhandbook.com/watch-logs-real-time/?ref=itsfoss.com) 可能会非常累人，特别是在你刚刚接触时。它全都是黑白的，而你得在其中寻找你需要的细节。这不是一个美丽的画面，对吧？

虽然我无法为你改变日志，但我可以向你展示一种使它们看起来更好、更易于阅读的方法。

你可能会问怎么做。[Tailspin](https://github.com/bensadeh/tailspin?ref=itsfoss.com) 就是我的答案。它是一个日志文件高亮显示器，它可以高亮显示日期、数字和严重性关键词（警告、信息、错误）等。

没错，它是用 Rust 编写的。 🦀

在本教程中，我将引导你了解如何安装和使用 Tailspin 工具，以丰富你的日志甚至是文本文件阅读体验。

## “让我为你的日志增添色彩” - Tailspin

{% image https://static.fosscope.com/articles_img/2024/03/tailspin/tailspin-on-different-log-files.webp "Tailspin 处理不同的日志文件" %}

与其他采用不同语法的现代 Linux 命令不同的是，你不需要从头开始重新学习全部东西就能使用 Tailspin。

它只是为你的日志/文本文件添加颜色，这样以来你可以立即发现关键元素。

最棒的是，你不需要任何额外的配置，它开箱即用。

### Tailspin 的关键特性

- 输出彩色的日志
- 搜索关键词
- 实时监控文件夹
- 可自定义颜色
- 使用 less 作为分页器，所以应当有大部分 less 命令的功能

现在，让我们来看看如何安装 Tailspin 工具。

## 如何在 Linux 中安装 Tailspin

Tailspin 在 Arch Linux 和 NixOS 的默认仓库中可用。但如果它不适用于你的发行版，我还会分享一种通过通用包管理器来安装它的方法。

**对于 Arch Linux：**

```
sudo pacman -S tailspin
```

**对于 Nix：**

```
nix-shell -p tailspin
```

如果你不使用 Arch 或 Nix 包管理器，那么你可以使用 Homebrew 或 cargo 包管理器。

根据我的个人经验，我推荐[使用cargo包管理器](https://itsfoss.com/install-rust-cargo-ubuntu-linux/)而不是 Homebrew，但这完全取决于你。

对于 cargo 包管理器：

```
cargo install tailspin
```

对于 [Homebrew](https://itsfoss.com/homebrew-linux/) 包管理器：

```
brew install tailspin
```

安装完成后，让我们看看如何来使用 Tailspin。

## 如何使用 Tailspin 工具

在这一节，我将通过各种示例引导你使用 Tailspin 工具。让我们从最明显的一个开始。

### 1. 使用 Tailspin 来获取彩色的日志

要使用 Tailspin 工具获取文本/日志文件的彩色输出，你所要做的就是将文件名附加到`tspin`命令上 **（tspin 是 tailspin 的二进制文件的名称）**：

```
tspin <Filename>
```

![](https://static.fosscope.com/articles_img/2024/03/tailspin/Use-the-tspin-command-to-show-log-file-in-colored-format.webp)

### 2. 实时监控目录/文件

Tailspin 工具允许你实时监控目录/文件，以了解哪些行正在被写入文件。

在我看来，监控特定文件比监控整个目录更有帮助，原因在于：

当你监控一个文件夹时，它显示的是文件夹正在发生的变化，但它不会指明哪个文件正在被修改。

但无论如何，我将引导你了解两种方式：监控目录和文件。

##### 监控目录

要监控目录，请将目录名称附加到`tspin`命令上：

```
tspin <directory>
```

![](https://static.fosscope.com/articles_img/2024/03/tailspin/Monitor-folders-in-real-time-using-tspin-command.gif)

在左侧，我对日志目录使用了`tspin`命令；在右侧，我编辑了两次`File1.txt`文件，从而让你明白在监控目录时应该预期什么。

如你所见，它并没有显示文件名，这就是为什么我更喜欢监控文件本身而不是整个目录。

##### 监控文件

要监控文件，请将文件名附加到`tspin`命令上，它将等待数据被写入指定的文件。一旦你写入任何更改，它将立即显示被写入到该文件中的行：

```
tspin <Filename>
```

![](https://static.fosscope.com/articles_img/2024/03/tailspin/monitor-file-changes-actively-using-the-tspin-command.gif)

似曾相识？是的，当你[使用 less 命令监控文件](https://linuxhandbook.com/watch-logs-real-time/?ref=itsfoss.com)时，它看起来完全一样，因为它使用 less 命令作为文件分页器。

### 3. 搜索关键词

要搜索关键词，用`tspin`命令打开一个文件，然后按正斜杠（/）并输入你要查找的关键词。

例如，在这里，我搜索了`User`词语，它将高亮显示匹配的结果：

![](https://static.fosscope.com/articles_img/2024/03/tailspin/Search-for-the-keyword-using-the-tspin-command.gif)

### 4. 通过管道与其他命令一起使用

到目前为止，我已经解释了如何对其他文件使用`tspin`命令，但它也可以用于标准输出。

你所要做的就是通过管道将`tspin`命令与你的实际命令一起使用，它会像对日志文件那样高亮显示输出的内容：

```
<command> | tspin
```

例如，这里我通过管道将`tspin`命令与`journalctl`命令一起使用：

```
journalctl -f | tspin
```

![](https://static.fosscope.com/articles_img/2024/03/tailspin/Search-for-the-keyword-using-the-tspin-command-1.gif)

### 5. 选择特定颜色来高亮显示某些关键词

Tailspin 工具在使用时采用预定义的颜色，但它也允许你指定对哪些元素应用哪些颜色。

为此，你需要使用`--print`标志，并按如下所示使用`--words-<color>`标志来指定颜色：

```
tspin <Filename> --print --words-<color> <keyword>
```

例如，在这里，我使用红色高亮显示`popcorn`词语，并使用黄色高亮显示`movie`词语：

```
tspin test.log --print --words-red popcorn --words-yellow movie
```

![](https://static.fosscope.com/articles_img/2024/03/tailspin/Use-a-specific-color-to-highlight-a-specific-keyword.webp)

## 总结...

我使用 Tailspin 工具通过用亮色高亮显示关键词来找到它。当然，编写这样长的命令并不是一个可行的选择，这就是为什么[我为了提高效率创建了一个别名](https://linuxhandbook.com/linux-alias-command/?ref=itsfoss.com)。

我希望你和我一样喜欢这个工具。如果你需要任何有关这个工具的进一步帮助，欢迎留言给我们。
