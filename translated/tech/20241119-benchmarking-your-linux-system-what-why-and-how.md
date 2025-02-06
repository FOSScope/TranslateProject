---
title: "对 Linux 系统进行基准测试：是什么、为什么以及怎么做"
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - cysnies
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/11/Benchmark-linux-system.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/11/Benchmark-linux-system.png
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://itsfoss.com/benchmark-tools-linux/

  作者：[Ankush Das](https://itsfoss.com/author/ankush/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[cysnies](https://github.com/cysnies)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: true # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

对 Linux 系统进行基准测试很简单，你只需要合适的工具。我们将在这里为你介绍这些工具。

<!-- more -->

如果你在使用 Linux 系统，系统性能不佳的情况是很少见的。

但是，「*有多快呢？*」这是我们在比较使用体验时经常会问自己或思考的问题。

要了解这一点，简单而有效的方法就是 **对 Linux 系统进行基准测试**。

*那么，该怎么做呢？* **当然是使用一些基准测试工具。** *那在 Linux 上有哪些可用的基准测试工具呢？*

别担心，在本文中，我将为你介绍一些工具，你可以使用它们针对各种用例对 Linux 系统进行基准测试。

{% note color:yellow ✋ "基准测试并不能完全反映系统的情况。在比较或评估系统性能时，它只是其中的一部分。<br/>要确保系统运行最佳，你需要正确的驱动程序、最新的软件、注重性能的桌面环境、稳定的内核以及其他一些因素。" %}

## 如何评估基准测试结果？

使用每个基准测试工具时，最终都会得到一个分数。

除非你心中有一个比较的标准，否则这个分数本身并没有什么意义。

你可以在两个不同的系统上进行基准测试，以衡量它们之间的性能差距。或者，你可以在不同的时间间隔对同一个系统进行基准测试，以检查配置更改或系统更新是否对性能产生了影响。

{% image https://itsfoss.com/content/images/2024/11/hp-laptop-benchmark-1.png '' %}

{% image https://itsfoss.com/content/images/2024/11/geekbench-scores.webp '' %}

搭载 AMD Ryzen 3 5300U 的笔记本电脑（Ubuntu 系统）与搭载 Intel i5 - 11600k 的台式机（Archcraft 系统）的 Geekbench 分数对比

例如，你可以在首次设置系统后立即进行基准测试，然后在几个月后再次测试。

有些工具还会提供一个排行榜，你可以在上面看到各种硬件配置的系统的得分。你可能还会发现它们提到了一个「**基线**」，这是特定硬件的参考分数。

例如，Geekbench 使用 2500 作为基线分数，这是针对 i7 - 12700 处理器的。据此，你可以知道自己的 CPU 性能是更好还是更差。

无论哪种情况，你都可以查看 Geekbench 网站上的 [所有处理器排名](https://browser.geekbench.com/processor-benchmarks)，然后将其与你的得分进行比较。

{% image https://itsfoss.com/content/images/2024/11/geekbench-processor-benchmarks.jpg '' %}

**建议在比较多个系统时使用相同的基准测试工具。**

## 4 款可帮助你对 Linux 计算机进行基准测试的工具

有些基准测试工具是开源的，而有些则不是。有些工具可以作为独立工具快速进行检查，而有些则可以帮助你对系统进行深入分析（不过并非所有人都需要这种分析）。

我将列出一些最好的工具，帮助你完成这项工作。

{% note color:cyan 📋 大多数基准测试工具都是基于命令行界面（CLI）的。 %}

### 1. UnixBench

{% image https://itsfoss.com/content/images/2024/11/unixbench-home.png '' %}

{% note color:green "<b>主要特性：</b>" <ul><li>传统测试</li><li>开源</li><li>易于使用</li><ul> %}

最传统的开源基准测试套件之一是 [UnixBench](https://github.com/kdlucas/byte-unixbench)。

它源自 1983 年开发的原始 BYTE UNIX 基准测试应用程序，多年来经过了多次修订和维护。它可能不是最现代的解决方案，但它执行的基本测试长期以来一直被证明是衡量性能的指标。

它提供了大约十种不同的测试，包括 **基本 2D/3D 图形**、**进程创建**、**字符串处理**、**浮点运算**、**文件复制** 等。

如果你不理解它所执行的测试的含义也没关系。你只需要知道它会对整个系统（*而不仅仅是系统的一部分*）进行一种压力测试。因此，测试结果将取决于操作系统、库、硬件和编译器。

安装完成后，你只需输入以下命令即可运行它：

```
ubench
```

以下是测试结果的样子：

{% image https://itsfoss.com/content/images/size/w2400/2024/11/unixbench-results.png '' %}

{% image https://itsfoss.com/content/images/2024/11/unixbench-result-1.png '' %}

从截图中可以看到，随着测试的进行（和完成），你可以在指定目录（*usr/lib/unixbench/results*）获取详细信息。你应该能找到 HTML 和日志文件，选择你熟悉的格式进行查看。

{% image https://itsfoss.com/content/images/2024/11/unixbench-result-files.png '' %}

你可以通过 [Arch Linux 的 AUR](https://itsfoss.com/aur-arch-linux/) 安装它。对于基于 Ubuntu 的发行版，它可以作为 [Snap](https://snapcraft.io/install/unixbench/ubuntu) 进行安装。

{% note color:cyan 💭 UnixBench 可能是较旧一代的基准测试工具，但它具有技术测试和开源的优势。无需进行复杂的设置，安装后只需输入一个命令即可开始基准测试，就是这么简单！ %}

<center>{% button "UnixBench" https://github.com/kdlucas/byte-unixbench %}</center>

### 2. Geekbench

{% image https://itsfoss.com/content/images/2024/11/geekbench-scores.png '' %}

{% note color:green "<b>主要特性：</b>" <ul><li>现代基准测试套件</li><li>跨平台</li><li>专有软件</li><li>可直接将结果上传到 Geekbench 网站</li><ul> %}

如果你想要一个现代的工具来对整个系统进行基准测试，并且不介意它不是开源的，那么 [Geekbench](https://www.geekbench.com/) 是最受欢迎的选择之一。

Linux 发行版没有可用的二进制文件。不过，你只需下载一个 **tar.gz** 文件，然后在解压后的文件夹中通过终端运行可执行文件（*无需使用 sudo*），命令如下：

```
./geekbench_x86_64
```

对我来说，它运行得非常顺利。

{% image https://itsfoss.com/content/images/2024/11/geekbench.png '' %}

{% image https://itsfoss.com/content/images/2024/11/geekbench-running.png '' %}

它会自动开始运行单核和多核测试，如光线追踪、文件压缩、HTML5 浏览器测试、PDF 渲染器等。在我的测试中，完成这些测试大约需要 2 - 5 分钟。

你只需点击提供的 URL 即可查看测试结果。

{% note color:cyan 💭 除非你使用的是 Geekbench 的专业版，否则进行测试需要有活跃的互联网连接。因此，它会将测试结果上传到其网站，并为你提供一个 URL 来查看结果。如果你不介意上传测试结果，这将是一次不错的体验。 %}

<center>{% button "Geekbench" https://www.geekbench.com/ %}</center>

### 3. Hardinfo2

{% image https://itsfoss.com/content/images/2024/11/hardinfo2.png '' %}

{% note color:green "<b>主要特性：</b>" <ul><li>图形用户界面</li><li>开源</li><li>易于使用</li><ul> %}

[Hardinfo2](https://github.com/hardinfo2/hardinfo2) 是一个多功能工具，你可以使用它 [获取系统网络、固件和硬件的基本信息](https://itsfoss.com/hardinfo/)。当然，它也允许你运行基准测试。

与上述两个工具不同，它不会直接进行全面的基准测试，而是允许你选择要测试的项目（CPU/内存/存储/图形）。

{% image https://itsfoss.com/content/images/2024/11/hardinfo2-benchmark.png '' %}

{% image https://itsfoss.com/content/images/2024/11/hardinfo2-result-generate.png '' %}

{% image https://itsfoss.com/content/images/2024/11/hardinfo2-result.png '' %}

而且，它是一个完整的图形界面程序。因此，你无需输入任何命令。只需选择你要执行的测试，完成后，它将显示测试结果，并与其他硬件进行参考排名比较。

你可以选择为所有执行的基准测试生成一份报告（HTML 文件），并单独查看。

我在 Arch Linux 上通过 AUR 安装了它。你可以在默认的 Linux 软件仓库中找到它。无论哪种方式，你都可以根据其 GitHub 页面上的说明从源代码进行编译安装。

{% note color:cyan 💭 Hardinfo2 是一款出色的以图形界面为中心的基准测试工具。测试完成速度快，并且可以轻松测试系统的各个部分。别忘了，你还可以使用这个工具获取系统的基本信息，因此测试完成后你可能还想保留它。 %}

<center>{% button "Hardinfo2" https://github.com/hardinfo2/hardinfo2 %}</center>

### 4. Phoronix Test Suite

{% image https://itsfoss.com/content/images/2024/11/phoronix-test-suite.png '' %}

{% note color:green "<b>主要特性：</b>" <ul><li>跨平台</li><li>开源</li><li>为高级用户提供全面的测试</li><ul> %}

最先进（且实用）的基准测试应用程序之一是 [Phoronix Test Suite](https://www.phoronix-test-suite.com/)。虽然它可用于所有平台，但在 Linux 上你可以体验到其完整的功能集，因为它是专门为 Linux 量身定制的。

它有大量可根据你的需求安装的工具。例如，你可以在 Phoronix Test Suite 中安装 Geekbench。当然，在我们的使用场景中，这有点多余。

我首先需要安装该套件，然后安装我想要执行的测试，最后运行它们。

安装测试并运行的命令如下（*忽略带有 # 的注释内容*）：

```
phoronix-test-suite install pts/sysbench # 安装
phoronix-test-suite run pts/sysbench # 运行
```

{% image https://itsfoss.com/content/images/2024/11/phoronix-sys-bench-run.png '' %}

{% image https://itsfoss.com/content/images/2024/11/phoronix-pybench.png '' %}

{% image https://itsfoss.com/content/images/2024/11/phoronix-sysbench.png '' %}

不幸的是，像 pts/browsers 这样的一些测试失败了，而 [**pybench**](https://github.com/lucianmarin/pybench)（*受 Geekbench 启发的基准测试工具*）和 [**sysbench**](https://github.com/akopytov/sysbench)（*开源基准测试工具*）测试运行得非常顺利。如果你希望使用一组工具（而不仅仅局限于一种）来测试系统的各个方面，那么 Phoronix Test Suite 适合你。

此外，它使用 [OpenBenchmarking.org](http://openbenchmarking.org/)，你可以将测试结果上传到该网站，并与其他硬件组合进行详细比较。

你可以通过 Arch Linux 的 AUR 以 **phoronix-test-suite** 为包名进行安装，或者从其 [GitHub 发布页面](https://github.com/phoronix-test-suite/phoronix-test-suite/releases) 下载 deb 包，用于基于 Ubuntu 的发行版。

{% note color:cyan 💭 与 Hardinfo2 不同，它是基于命令行界面的。但是，当你开始测试时，它会为你提供各种交互式选项。例如，*是否要保存报告*、*系统名称* 等等。如果你正确遵循其文档说明，就可以对系统进行全面的分析。 %}

## 你真的需要进行基准测试吗？

这取决于你的需求，但基准测试可以让你了解计算机在操作系统下的性能表现。

例如，当 [我从 Ubuntu 切换到 Archcraft](https://news.itsfoss.com/archcraft-experience/) 时，我注意到了一些性能提升。在我的情况下，有一些直观的指标可以证明这一点。

但在很多情况下，除非你大量使用并跟踪文件提取时间、启动时间、CPU 性能以及其他资源效率/使用统计数据，否则很难轻易衡量出差异。

同样，也许你正在切换到另一个发行版，想检查性能差异。或者，你刚刚组装了一台新电脑，想在开始使用之前先测试一下。

在这些情况下，对 Linux 进行基准测试会很有帮助。

💬 *你会对系统进行基准测试吗？请在下面的评论中分享你的想法！*