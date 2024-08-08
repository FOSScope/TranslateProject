---
title: Fractal 8 Released: The Linux Matrix Messaging App Gets Better!
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/fractal-8-released-the-linux-matrix-messaging-app-gets-better/fractal-8-release.png
cover: https://static.fosscope.com/articles_img/2024/08/fractal-8-released-the-linux-matrix-messaging-app-gets-better/fractal-8-release.png
categories:
  - 翻译
  - 新闻
tags: 
  - Matrix
authorInfo: |
  via: https://news.itsfoss.com/fractal-8-release/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出

---

A new upgrade has landed for Matrix users!

<!-- more -->

Fractal is undoubtedly one of the [best Matrix clients for decentralized messaging](https://itsfoss.com/best-matrix-clients/) around. Even though it's tailored for the GNOME desktop environment, its features and portability ensure that it can be used on most popular Linux distros comfortably.

Did I mention it's [Rust](https://itsfoss.com/tag/rust-basics/)-based?

Well, its developers have recently introduced a new release that features some important quality-of-life upgrades.

Let's take a look without further ado. 😃

## 🆕 Fractal 8: What's New?

![a screenshot of fractal 8 with the official matrix room of fedora open](https://static.fosscope.com/articles_img/2024/08/fractal-8-released-the-linux-matrix-messaging-app-gets-better/Fractal_8-1.png)

We start off with the upgrades to drafts. **Unsent typed messages are now stored separately, on a room-by-room basis**, and are not lost on application restart. The latter was made possible by due to tweaks in the database code.

Similarly, there is now support for authenticated media, **improvements to the mention behavior (sent intentionally)**, fixes for the history media viewers, a new banner that shows up when synchronization with a homeserver fails, and a streamlined verification and account recovery process.

The developers have also brought about **persistence for collapsed categories in the sidebar** across application/system restarts, with the “*Historical*” category being collapsed by default.

Additionally, they have implemented more robust HTML rendering, and **code blocks now have support for syntax highlighting**. Lists also see some useful refinements, with those now having the ability to be nested, and numbered lists being able to start with a random number.

## 📥 Download Fractal 8

The most straightforward way to get this release of Fractal is by getting it from the [Flathub store](https://flathub.org/apps/org.gnome.Fractal). If you are interested in the source code, then head to its [GitLab](https://gitlab.gnome.org/World/fractal) repo.

<center>{% button "Fractal 8 (Flathub Store)" https://flathub.org/apps/org.gnome.Fractal %}</center>
