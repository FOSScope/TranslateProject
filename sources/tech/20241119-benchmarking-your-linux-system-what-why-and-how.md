---
title: Benchmarking Your Linux System: What, Why and How
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://itsfoss.com/benchmark-tools-linux/

  作者：[Ankush Das](https://itsfoss.com/author/ankush/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: false # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

It is easy to benchmark your Linux system, you just need the right tools. We tell you about those here.

<!-- more -->

If you are using Linux on your system, it is a rare phenomenon that your system is not performing well.

But, "*how fast?*" is a question that we often ask ourselves or wonder when thinking to compare our experiences.

The easy and effective solution to know that is to **benchmark your Linux system**.

*So, how do you do that?* **Using some benchmarking tools.** *And, what are the benchmarking tools available on Linux?*

Fret not, in this article, I shall guide you with the tools with which you can perform a Linux system benchmark for all kinds of use-cases.

{% note color:yellow ✋ "Benchmarking is not the complete story. But, only a part of it when comparing or evaluating the performance of a system.<br/>To ensure your system runs the best, you need the correct drivers, up-to-date software, performance-focused desktop environment, a stable kernel, and a few other things." %}

## How to evaluate the benchmark results?

With every benchmark tool, you end up getting a final score.

The score alone is not meaningful unless you have a comparison in mind.

You can either perform benchmarks on two different systems to measure the performance gap. Or, you can benchmark the same system at different time intervals to check if a configuration/system update impacted the performance in any way.

<img alt="" height="849" width="1411" />\<img src="https://itsfoss.com/content/images/2024/11/hp-laptop-benchmark-1.png" width="1411" height="849" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/hp-laptop-benchmark-1.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/hp-laptop-benchmark-1.png 1000w, https://itsfoss.com/content/images/2024/11/hp-laptop-benchmark-1.png 1411w" sizes="(min-width: 720px) 720px"\>

<img alt="" src="https://itsfoss.com/content/images/2024/11/geekbench-scores.webp" height="856" width="1342" />

Geekbench scores for a laptop with AMD Ryzen 3 5300U (Ubuntu) vs desktop with an Intel i5-11600k (Archcraft)

For example, you benchmark the system right after you set it up for the first time, and then after a few months.

Some tools also provide you with access to a leaderboard chart, where you can see scores of systems with various hardware configurations. You may also find them mention a "**baseline**" which is a reference score of a particular hardware.

For instance, Geekbench utilizes 2500 as baseline score, which is for an i7-12700 processor. You can know if your CPU performs better or worse accordingly.

In either case, you can check the Geekbench website that [ranks all processors](https://browser.geekbench.com/processor-benchmarks), and then compare it against your score.

<img alt="a screenshot of geekbench processor leaderboard" height="857" width="1054" />\<img src="https://itsfoss.com/content/images/2024/11/geekbench-processor-benchmarks.jpg" class="kg-image" alt="a screenshot of geekbench processor leaderboard" loading="lazy" width="1054" height="857" srcset="https://itsfoss.com/content/images/size/w600/2024/11/geekbench-processor-benchmarks.jpg 600w, https://itsfoss.com/content/images/size/w1000/2024/11/geekbench-processor-benchmarks.jpg 1000w, https://itsfoss.com/content/images/2024/11/geekbench-processor-benchmarks.jpg 1054w" sizes="(min-width: 720px) 720px"\>

**It is recommended to use the same benchmark test/tool when comparing multiple systems.**

## 4 tools that can help you benchmark your Linux computer

Some benchmarking tools are open source, while a few are not. Some are available as a standalone tool for a quick check, and some help you take an in-depth analysis of your system (which is not needed for everyone).

I list the best ones to help you get the job done.

{% note color:cyan 📋 Most of the benchmarking tools are CLI-based. %}

### 1. UnixBench

<img alt="a screenshot of unixbench utility" height="572" width="883" />\<img src="https://itsfoss.com/content/images/2024/11/unixbench-home.png" class="kg-image" alt="a screenshot of unixbench utility" loading="lazy" width="883" height="572" srcset="https://itsfoss.com/content/images/size/w600/2024/11/unixbench-home.png 600w, https://itsfoss.com/content/images/2024/11/unixbench-home.png 883w" sizes="(min-width: 720px) 720px"\>

{% note color:green "<b>Key Features:</b>" <ul><li>Traditional test</li><li>Open Source</li><li>Easy to Use</li><ul> %}

One of the most traditional open source benchmark suite is [UnixBench](https://github.com/kdlucas/byte-unixbench).

It is derived from the original BYTE UNIX benchmark app built back in 1983, and has been maintained over the years with several revisions. It may not be the most modern solution out there, but it performs essential tests that have been long proven to be indicators of performance.

You get around ten different tests which include **basic 2D/3D graphics**, **process creation**, **string handling**, **floating-point operations**, **file copy**, and a couple of others.

It is alright if you do not understand the meaning of the tests it performs. All you need to know is that it performs a type of stress test of your entire system (*not just a part of it*). So, the results will depend on the operating system, libraries, hardware, and compiler.

Once installed, you just have to run it by typing the following command:

```
ubench
```

Here's how the results look:

<img alt="" height="486" width="2000" />\<img src="https://itsfoss.com/content/images/2024/11/unixbench-results.png" width="2000" height="486" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/unixbench-results.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/unixbench-results.png 1000w, https://itsfoss.com/content/images/size/w1600/2024/11/unixbench-results.png 1600w, https://itsfoss.com/content/images/size/w2400/2024/11/unixbench-results.png 2400w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="1110" width="1260" />\<img src="https://itsfoss.com/content/images/2024/11/unixbench-result-1.png" width="1260" height="1110" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/unixbench-result-1.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/unixbench-result-1.png 1000w, https://itsfoss.com/content/images/2024/11/unixbench-result-1.png 1260w" sizes="(min-width: 720px) 720px"\>

Click on the images to expand

As you can see in the screenshots, as the test progresses (and completes), you can head to the mention directory (*usr/lib/unixbench/results*) to get the details. You should find HTML and log files, access what you are comfortable with.

<img alt="" height="299" width="811" />\<img src="https://itsfoss.com/content/images/2024/11/unixbench-result-files.png" class="kg-image" alt="" loading="lazy" width="811" height="299" srcset="https://itsfoss.com/content/images/size/w600/2024/11/unixbench-result-files.png 600w, https://itsfoss.com/content/images/2024/11/unixbench-result-files.png 811w" sizes="(min-width: 720px) 720px"\>

You can install it via [AUR for Arch Linux](https://itsfoss.com/aur-arch-linux/). And, for Ubuntu-based distros, it is available as a [Snap](https://snapcraft.io/install/unixbench/ubuntu).

{% note color:cyan 💭 UnixBench could be an older generation of benchmarking tests, but it has its benefits of technical testing and being an open source tool. No options to fiddle around, just type in one command after installation to start benchmarking, it is that easy! %}

<center>{% button "UnixBench" https://github.com/kdlucas/byte-unixbench %}</center>

### 2. Geekbench

<img alt="a screenshot of geekbench test result" height="856" width="1342" />\<img src="https://itsfoss.com/content/images/2024/11/geekbench-scores.png" class="kg-image" alt="a screenshot of geekbench test result" loading="lazy" width="1342" height="856" srcset="https://itsfoss.com/content/images/size/w600/2024/11/geekbench-scores.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/geekbench-scores.png 1000w, https://itsfoss.com/content/images/2024/11/geekbench-scores.png 1342w" sizes="(min-width: 720px) 720px"\>

{% note color:green "<b>Key Features:</b>" <ul><li>Modern benchmark suite</li><li>Cross-Platform </li><li>Proprietary</li><li>Uploads results to Geekbench website directly</li><ul> %}

If you want a modern tool to benchmark your entire system and do not mind if it is not open source, [Geekbench](https://www.geekbench.com/) is one of the most popular option.

There is no binary available for Linux distros. However, you just have to download a **tar.gz** file and run the executable via the terminal (*no need of sudo*) using the following command inside the extracted folder:

```
./geekbench_x86_64
```

It worked like charm for me.

<img alt="" height="702" width="1107" />\<img src="https://itsfoss.com/content/images/2024/11/geekbench.png" width="1107" height="702" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/geekbench.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/geekbench.png 1000w, https://itsfoss.com/content/images/2024/11/geekbench.png 1107w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="702" width="1107" />\<img src="https://itsfoss.com/content/images/2024/11/geekbench-running.png" width="1107" height="702" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/geekbench-running.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/geekbench-running.png 1000w, https://itsfoss.com/content/images/2024/11/geekbench-running.png 1107w" sizes="(min-width: 720px) 720px"\>

It will automatically start running single-core, and multicore tests like Ray Tracer, File Compression, HTML5 browser test, PDF Renderer, and several others. In my testing, it took around 2–5 minutes to complete.

All you have to do is click on the URL provided to check your results.

{% note color:cyan 💭 Geekbench testing requires an active internet connection unless you have its Pro edition. So, it uploads the results to its website, and gives you a URL to check the result. It is a neat experience if you do not mind uploading your results. %}

<center>{% button "Geekbench" https://www.geekbench.com/ %}</center>

### 3. Hardinfo2

<img alt="" height="844" width="1284" />\<img src="https://itsfoss.com/content/images/2024/11/hardinfo2.png" class="kg-image" alt="" loading="lazy" width="1284" height="844" srcset="https://itsfoss.com/content/images/size/w600/2024/11/hardinfo2.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/hardinfo2.png 1000w, https://itsfoss.com/content/images/2024/11/hardinfo2.png 1284w" sizes="(min-width: 720px) 720px"\>

{% note color:green "<b>Key Features:</b>" <ul><li>Graphical User Interface</li><li>Open Source</li><li>Easy to Use</li><ul> %}

[Hardinfo2](https://github.com/hardinfo2/hardinfo2) is a multipurpose tool with which you can[ get essential information on your system's network, firmware, and hardware](https://itsfoss.com/hardinfo/). And, of course, it lets you run benchmarks.

Unlike the above two tools, it does not perform a complete benchmark, but allows you to choose what to test (CPU/Memory/Storage/Graphics).

<img alt="" height="844" width="1284" />\<img src="https://itsfoss.com/content/images/2024/11/hardinfo2-benchmark.png" width="1284" height="844" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/hardinfo2-benchmark.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/hardinfo2-benchmark.png 1000w, https://itsfoss.com/content/images/2024/11/hardinfo2-benchmark.png 1284w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="847" width="1297" />\<img src="https://itsfoss.com/content/images/2024/11/hardinfo2-result-generate.png" width="1297" height="847" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/hardinfo2-result-generate.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/hardinfo2-result-generate.png 1000w, https://itsfoss.com/content/images/2024/11/hardinfo2-result-generate.png 1297w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="778" width="2000" />\<img src="https://itsfoss.com/content/images/2024/11/hardinfo2-result.png" width="2000" height="778" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/hardinfo2-result.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/hardinfo2-result.png 1000w, https://itsfoss.com/content/images/size/w1600/2024/11/hardinfo2-result.png 1600w, https://itsfoss.com/content/images/2024/11/hardinfo2-result.png 2317w" sizes="(min-width: 720px) 720px"\>

Click to expand images

And, it is a complete GUI program. So, you do not need type any commands. Just head to the test you want to perform, and once it is done, it will show you the result along with a reference ranking compared to other hardware.

You can decide to generate a report for all the benchmarks you perform (HTML file) and access it separately.

I installed it via AUR on Arch Linux. You can find it in your default Linux repositories. In either case, you can build it from source using the instructions on its GitHub page.

{% note color:cyan 💭 Hardinfo2 is a wondering GUI-focused benchmarking tool. The tests finish up fast, and it is easy to test all kinds of parts in your system. Not to forget, you can get essential system information with this tool, so you will want to keep it around after testing. %}

<center>{% button "Hardinfo2" https://github.com/hardinfo2/hardinfo2 %}</center>

### 4. Phoronix Test Suite

<img alt="phoronix test suite" height="702" width="1107" />\<img src="https://itsfoss.com/content/images/2024/11/phoronix-test-suite.png" class="kg-image" alt="phoronix test suite" loading="lazy" width="1107" height="702" srcset="https://itsfoss.com/content/images/size/w600/2024/11/phoronix-test-suite.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/phoronix-test-suite.png 1000w, https://itsfoss.com/content/images/2024/11/phoronix-test-suite.png 1107w" sizes="(min-width: 720px) 720px"\>

{% note color:green "<b>Key Features:</b>" <ul><li>Cross-Platform</li><li>Open Source</li><li>Comprehensive tests for advanced users</li><ul> %}

One of the most advanced (and useful) benchmark applications is the [Phoronix Test Suite](https://www.phoronix-test-suite.com/). While it is available for all platforms, you can expect the full feature-set on Linux, for which it is tailored for.

It has a massive collection of tools that are installable, as per your requirements. For instance, you can install Geekbench from within the Phoronix Test Suite. Of course, that is a bit redundant in our use-case.

I had to install the suite first, then the test(s) I wanted to perform, and then run them.

The command for installing a test and running it looks like (*ignore words with #*):

```
phoronix-test-suite install pts/sysbench #installing
phoronix-test-suite run pts/sysbench #running
```

<img alt="" height="572" width="883" />\<img src="https://itsfoss.com/content/images/2024/11/phoronix-sys-bench-run.png" width="883" height="572" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/phoronix-sys-bench-run.png 600w, https://itsfoss.com/content/images/2024/11/phoronix-sys-bench-run.png 883w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="572" width="883" />\<img src="https://itsfoss.com/content/images/2024/11/phoronix-pybench.png" width="883" height="572" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/phoronix-pybench.png 600w, https://itsfoss.com/content/images/2024/11/phoronix-pybench.png 883w" sizes="(min-width: 720px) 720px"\>

<img alt="" height="1067" width="1635" />\<img src="https://itsfoss.com/content/images/2024/11/phoronix-sysbench.png" width="1635" height="1067" loading="lazy" alt="" srcset="https://itsfoss.com/content/images/size/w600/2024/11/phoronix-sysbench.png 600w, https://itsfoss.com/content/images/size/w1000/2024/11/phoronix-sysbench.png 1000w, https://itsfoss.com/content/images/size/w1600/2024/11/phoronix-sysbench.png 1600w, https://itsfoss.com/content/images/2024/11/phoronix-sysbench.png 1635w" sizes="(min-width: 720px) 720px"\>

Unfortunately, some tests like pts/browsers failed, while [**pybench**](https://github.com/lucianmarin/pybench) (*benchmark inspired by geekbench*) and [**sysbenc**](https://github.com/akopytov/sysbench)**h** (*open source benchmark*) tests worked like charm. If you wish to test various aspects of your system using a set of tools (not just limited to one), Phoronix Test Suite is for you.

Moreover, it makes use of [OpenBenchmarking.org](http://openbenchmarking.org/) to which you can upload your test results, and compare it with great details with other combination of hardware.

You can install the suite via AUR for Arch Linux with **phoronix-test-suite** as the package name or download the deb package from its [GitHub releases](https://github.com/phoronix-test-suite/phoronix-test-suite/releases) for Ubuntu-based distros.

{% note color:cyan 💭 Unlike hardinfo2, it is CLI-based. But, it gives you all kinds of interactive options when you start a test. Things like *if you want to save a report*, *the name of your system*, and more. If you follow its documentation correctly, you can perform a comprehensive analysis of your system. %}

## Do you really need benchmarking?

It depends on what you are looking for but benchmarking could give you some ideas about how your computer is performing with the operating system.

For instance, when [I switched from Ubuntu to Archcraft](https://news.itsfoss.com/archcraft-experience/), and I noticed a few performance improvements. In my case, there were visual indicators for me to say that.

But, in many scenarios, you cannot easily gauge the difference unless you extensively use/keep track of file extraction times, boot times, CPU performance, and other resource efficiency/usage stats.

Similarly, maybe you are switching to another distro, and want to check the performance difference. Or, perhaps, you just built a new computer, and want to test the waters before you start using it.

Benchmarking Linux can be helpful in such cases.

💬 *Do you perform a system benchmark? Let me know your thoughts in the comments below!*
