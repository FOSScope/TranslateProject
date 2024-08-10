---
title: Debian Developer Shares Plans to Improve APT
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/debian-developer-shares-plans-to-improve-apt/debian-apt.png
cover: https://static.fosscope.com/articles_img/2024/08/debian-developer-shares-plans-to-improve-apt/debian-apt.png
categories:
  - 翻译
  - 新闻
tags: 
  - Debian
  - APT
authorInfo: |
  via: https://news.itsfoss.com/debian-apt

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Some under-the-hood work that should make a good impact!

<!-- more -->

[APT](https://wiki.debian.org/Apt), short for Advanced Package Tool, is one of the most prevalent choices among all the different package managers, found mainly on [Debian](https://www.debian.org/) and other Debian-based distributions such as Ubuntu.

Since its introduction way back in 1998, APT has gotten better over the years, with constant patches being made to keep it relevant in the ever-evolving space of Linux-based distros.

A recent update saw the introduction of [APT 2.9.3](https://tracker.debian.org/news/1529821/accepted-apt-293-source-into-unstable/), which shipped with an experimental dependency solver called **Solver3**, that's aiming to become the default solver in the near future. Thanks to [The New Stack](https://thenewstack.io/debian-retools-apt-for-superior-dependency-management/), we now have a better look at what that might be like. 😃

Not to forget, we also got the new color, in case you missed it:

{% link https://news.itsfoss.com/apt-new-ui/ Finally! The New UI for APT Adds a Splash of Color to Improve Readability icon:https://static.fosscope.com/articles_img/2024/08/debian-developer-shares-plans-to-improve-apt/apt-new-release.png %}

## APT To Get A Boost: What to Expect?

{% image https://static.fosscope.com/articles_img/2024/08/debian-developer-shares-plans-to-improve-apt/Apt_2.7.14.png Just a stand-in image of APT %}

Speaking during [DebConf 24](https://wiki.debian.org/DebConf/24), Debian Developer,[ Julian Andres Klode](https://github.com/julian-klode) shared insights into how he had been working on the Solver3 project since 2010 during his spare time.

The [Solver3](https://blog.jak-linux.org/2024/05/14/solver3/) is a dependency solving algorithm for APT, that starts with an empty set of packages, progressively adding any manually installed packages, then automatically installing any missing ones to resolve dependencies.

Compared to that, Julian points out that **the current solver takes 45% of the total build time** for rebuilding the dependency tree on Intel systems.

When measured at scale, the numbers add up, and there's plenty of time that's wasted in carrying out such a menial task. The Solver3, according to him, just takes 15% of the build time, and results in a 40% improvement in build times compared to the existing solver in his testing.

**Before he could arrive at this solution**, he had to go through three different approaches for handling dependencies. First, he tried to procure an external solver from FreeBSD called “[picosat](https://cgit.freebsd.org/ports/tree/math/picosat)”, it didn't pan out owing to the many limitations of working with an external library.

Then, he tried describing the dependency tree as a “[pseudo-Boolean](https://en.wikipedia.org/wiki/Pseudo-Boolean_function)” optimization problem, with three methods being employed, all of which entailed issues such as package sizes, weird optimization, and dependence on [global optimization](https://en.wikipedia.org/wiki/Global_optimization).

And, finally, he tried a modular graph solver method, which was not used in the project, but did help with the outcome.

Of course, Julian does mention that **there's plenty of work to be done before this can be made the default**, he added that:

> This is going to be quite powerful, but we want to restrict it a bit to not pick solutions that actually don’t make sense. Packages for multiple architectures should be limited to only those architectures being used.

> Manually packages should only be removed upon explicit request, and a replacement package should designated when appropriate. Obsolete packages should also be considered only as a last choice.

He also feels that there's a need for more benchmarking to be done, comparing Solver3 with the existing solver once it is in production, and that he would also like to bring Solver3 closer to [MiniSat](http://minisat.se/).

### Want To Check It Out?

Currently, a beta release is planned as an opt-in for the upcoming Debian 13 “[Trixie](https://www.debian.org/releases/trixie/)” release, which is said to arrive around February 2025.

As for when Solver3 would be made the default solver, if everything goes as planned with the beta release, then the follow-up Debian 14 “[Forky](https://wiki.debian.org/DebianForky)” release is the prime candidate for it.

For an early look at Solver3's code, you can head to apt-pkg's main branch on Debian's [GitLab](https://salsa.debian.org/apt-team/apt/-/tree/main/apt-pkg) repo, where you can search for “*solver3*”.

<center>{% button "apt-pkg (GitLab)" https://salsa.debian.org/apt-team/apt/-/tree/main/apt-pkg %}</center>