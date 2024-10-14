---
title: 如何通过 Hacktoberfest 参与开源项目
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - Cubik65536
  - {{proofreader}}
banner: {{cover_image}}
cover: {{cover_image}}
categories:
  - 翻译
  - {{category}}
tags: {{tags}}
authorInfo: |
  via: https://itsfoss.com/hacktoberfest-guide/

  作者：[Pratham Patel](https://itsfoss.com/author/pratham/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[Cubik65536](https://github.com/Cubik65536)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: true # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

Hacktoberfest 是回馈开源项目的最佳场所。以下是你需要知道的关于 Hacktoberfest 的一切，以及如何参与其中...

<!-- more -->

开源项目以其[通常]良好的代码质量统治着世界，但更重要的是它们是免费提供的。这也意味着用户与贡献者的比例非常低。

换种说法来讲，与数以百万计的用户相比，只有几百名贡献者在维护/改进这些开源项目。

Hacktoberfest 是来自 [DigitalOcean](https://itsfoss.com/recommends/digital-ocean/) 的一个活动，鼓励你回馈你喜欢的项目。作为回报，你可以选择从 DigitalOcean 领取礼物，或者选择种一棵树。

![向 Hacktoberfest 贡献](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/contribute-to-hacktoberfest.webp)

## 谁可以参与 Hacktoberfest？

Hacktoberfest 2024 欢迎所有人参与。

你不需要是一个开发者或者计算机科学系学生。无论你是艺术家、作家还是翻译者，任何人都可以以某种方式回馈开源项目。

## 为什么你应该参与 Hacktoberfest？

通过 Hacktoberfest，DigitalOcean 试图提高人们对开源项目的认识。它旨在鼓励用户探索开源项目开发者的经历。

你也会意识到开发者投入了大量的时间、精力和心力，免费提供代码的价值。

**Hacktoberfest 活动鼓励你支持你喜欢的开源项目**。这样，你可以确保你喜欢的项目/工具不断改进，以满足你的需求。

归根结底，开源是关于社区努力和防止供应商锁定的。因此，你不能指望开发者为了你的利益而做所有的工作，对吧？

![hacktoberfest 2022](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/hacktoberfest-2022.webp)

**「但我能从中得到什么好处呢？」**

这个活动鼓励你**回馈**对你最有影响力的项目。这样做将确保项目得到其 bug 的修复和新功能的添加。不仅仅局限于你回馈的责任，更多的好处包括：

* 增加你的创造力。
* 体验开源项目开发背后的过程（这也有助于你的职业发展）。
* 收到 Hacktoberfest T 恤之类的礼物。

上述提到的好处只是几乎所有人都在谈论的。但其他好处也是有的。为开源项目做贡献将**改善你的作品集**，并告诉你的**未来雇主你可以与开源社区合作**。

它还可以帮助你了解如何在未来维护你的开源项目。如果你选择这样做，学习社区如何相互交流将帮助你塑造你或你雇主的开源项目，使其既有利于你，**又**有利于整个社区。

更不用说，接触来自世界各地的新人会让你以一种全新的方式了解「如何完成事情 X」。类似的经历可以帮助你在面对挑战性问题时跳出固有思维模式。

## 我可以为哪些项目做贡献？

![hacktoberfest 2022 question](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/hacktoberfest-2022-question.webp)

严格来讲，你可以为任何你想要的项目做贡献。但是，有一些项目与 Hacktoberfest 的价值观不符；为这些项目做贡献将不会计入你完成活动的总目标。

最好的方法是在 GitHub 或 GitLab 上查找带有「Hacktoberfest」标签的项目。

* 你可以在 [GitHub](https://github.com/topics/hacktoberfest) 上找到符合要求的仓库。
* 你可以在 [GitLab](https://gitlab.com/explore/projects/topics/hacktoberfest) 上找到符合要求的代码仓库。

请确保你要为之做贡献的项目有「Hacktoberfest」主题。对其他项目的贡献可能不会计入你的最终目标。

## 我可以做什么？如何开始？

First, please ensure that you have **registered for Hacktoberfest using your GitHub or GitLab account**.
首先，请确保你已经**使用你的 GitHub 或 GitLab 账户注册了 Hacktoberfest**。

[注册 Hacktoberfest](https://hacktoberfest.com/auth/)

**“但我不会编程，这没关系吗？”**

这完全没关系！参与开源并不意味着你必须知道如何编写代码。代码只是开源的一部分。开源项目可能需要许多东西。以下只是我想到的一些：

* **增加/修复代码**： 这是最明显的一种对开源项目的贡献方式。你可以提交 bug 修复、新功能，甚至修复安全问题。提交一个 Pull Reqwuest，实现你一直想要的功能！
* **改进文档**：文档对每个项目都至关重要。开发者需要阅读文档，用户也需要文档。你可以帮助改进/修复文档。
* **帮助翻译**：开源意味着全球任何人都可以访问你的项目。但这也意味着有些人可能无法阅读/写作/说英语。提供他们母语的翻译将促进合作。
* **创造视觉内容**：有些软件项目没有人能够创造出好的 Logo 等图形。你也可以帮助完成这些任务。
* **UI/UX 设计**：如果你无法提供图形设计，你可以帮助 UI/UX 设计。

你还可以帮忙宣传这个项目，与世界分享，提高其社交影响力。

**另外，如果你没有时间参与 Hacktoberfest，你也可以通过捐款来支持项目。**

[向项目捐款](https://hacktoberfest.com/donate/)

## 参与 Hacktoberfest 之前需要知道的事情

![hacktoberfest 2022 rules](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/hacktoberfest-2022-rules.webp)

参与 Hacktoberfest 很容易，但是要**完成 Hacktoberfest**（即“赢得 Hacktoberfest”），你需要知道其他一些事情：

* 你需要注册成为 Hacktoberfest 用户。
* 你在 [GitLab](https://gitlab.com/explore/projects/topics/hacktoberfest) 或者 [GitHub](https://github.com/topics/hacktoberfest) 上提交的 Pull Request 必须在 10 月 1 日至 10 月 31 日期间（包括这两天）提交。
* 你的至少**四个** Pull Request 必须在相应的仓库中被**合并或接受**。
* 你的 Pull Request 必须被提交到有「**Hacktoberfest**」标签的仓库中，或者它必须被标记为「**Hacktoberfest-accepted**」。

参与 2024 年的 Hacktoberfest 的人将获得一个来自 Holopin 的可定制的数字徽章，其每次提交/合并请求都会获得新的特性。在早期的 Hacktoberfest 版本中，你实际可以获得实体的纪念品和商品（如 T 恤/贴纸等），但人们开始通过提交虚假的 Pull Request 来获得这些奖励。

还有一些可能影响你参与的条件，包括：

* 多于两个被标记为「**spam**（垃圾）」的 Pull Request 将使你从本次 Hacktoberfest *和* **未来的 DigitalOcean 活动中被取消资格**。
* 任何被标记为「**Invalid**（无效）」（由维护者标记）的 Pull Request 将从你的总目标中被丢弃。
* 任何被提交到与 Hacktoberfest 的价值观不符的仓库的 Pull Request 将不会计入你的总目标。目前，没有官方列表通知你有关这样的仓库。如果不确定，请在[官方 Hacktoberfest Discord 服务器](https://discord.gg/hacktoberfest)上提问。
* 请避免提交只有*微小好处*或仅仅为了引入一个小改变的 Pull Request。例如：「*修复空格*」，「*修正拼写错误*」，「*使用空格重新格式化代码而不是制表符*」，以及「*从 0 递增到 i 而不是递减 i 到 0*」。

## 我如何知道项目的贡献指南？

![hacktoberfest 2022 dark](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/hacktoberfest-2022-dark.webp)

任何接受 Hacktoberfest Pull Request 的仓库都会有一个名为 **CONTRIBUTING.md** 的文件，其中包含了你第一次为该仓库做贡献所需的所有信息。

尽管我会在下一节讨论为项目做贡献的流程，但在继续之前，你应该查看每个项目的指南。

**CONTRIBUTING.md** 文件通常包含以下内容：

* **行为准则**：请**仔细**阅读。这是指个人在项目中的可接受行为。如果你没有遵守这一点，你未来的贡献可能会被忽视；甚至可能被直接拒绝。
* **代码格式**：每个项目都有自己的代码风格。最好根据 CONTRIBUTING.md 中列出的代码格式来格式化代码。
* **服务条款**：有些项目要求你在你的 Pull Request 被合并之前接受条款和条件（关于你对贡献代码的权利）。请仔细阅读这些内容，并确保你对限制（如果有的话）感到满意。
* **许可证**：请阅读仓库代码所使用的许可证。你必须遵守该许可证。
* **贡献者资源**：由于这个文件（CONTRIBUTING.md）是为首次进行贡献的贡献者准备的，你还将获得一些贡献者资源，帮助你了解代码审查是如何进行的，以及为了合并一个 Pull Request 需要做哪些事情。
* **PR 标签**：有些维护者希望你使用标签创建一个 Pull Request。这些标签可能是「bug 修复」，「新功能」，「好的首次问题」等。这有助于维护者和社区关注他们感兴趣的问题。
* **Issue 模板**：如果你发送一个 Pull Request，有时你需要运行一些命令。这些命令可能会做一些事情，比如「清理构建文件」，「删除自定义配置文件」等。
* **如何设置开发环境**：有时，CONTRIBUTING.md 文件还会列出构建软件项目所需的所有包。有的时候你还会被告知如何打包。这些内容将被包括在内，以便你在发送 Pull Request 之前测试你的更改是否会破坏某些东西。
* **所有权信息**：这一部分将包括诸如「X 处理 bug 修复的 Pull Request」之类的细节，因此如果你的 bug 修复 Pull Request 没有被接受，你可以向 X 询问意见，以及如何改进你的 Pull Request，使其被接受。

## 这整个过程是如何工作的？

现在你已经了解了前提条件。你该如何继续？如何提交你的第一个 Pull Request？对于第一次进行贡献的人来说，这是否太技术性了？

并不一定。你只需要输入几个命令，并仔细按照逐步方法操作。没有什么是令人不安的。你只需要耐心地完成整个过程。

整体来讲，你需要做的事情如下：

1. **安装和设置 Git。**
2. **创建一个 GitHub 或 GitLab 账户。**
3. **Fork 你想要贡献的仓库。**
4. **使用 Git 在仓库中工作。**
5. **将代码/更改提交到仓库。**

## How To Make Your First Pull Request?#
## 如何提交你的第一个 Pull Request？

不要害怕，我将按照正确的顺序为你提供所有步骤，帮你上手。

### 1. 在你的系统上安装 Git

![hacktoberfest 2022 git](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/hacktoberfest-2022-git.webp)

Git 是业界最常用的版本控制工具之一。它是由 Linus Torvalds 创建的。是的，就是那个创建了 Linux 的人。

在我告诉你 git 的基础用法之前，让我先告诉你如何在你的计算机上安装 git。

#### 在 Linux 上安装 git

使用基于 Debian/Ubuntu 的系统的用户可以使用 apt 包管理器安装 git，命令如下：

``` bash
sudo apt install git git-man
```

使用基于 Fedora/RHEL 的 Linux 发行版的用户可以使用 dnf 包管理器安装 git，命令如下：

``` bash
sudo dnf install git git-core git-core-doc
```

Arch Linux 用户可以使用 [pacman 包管理器](https://itsfoss.com/pacman-command/)安装 git，命令如下：

``` bash
sudo pacman -Sy git
```

#### 在 macOS 上安装 git

macOS 用户可以使用 `brew` 或 `macports` 包管理器安装 git。

``` bash
# Homebrew 用户
brew install git
# MacPorts 用户
sudo port install git
```

#### 在 Windows 上安装 git

希望在 Windows 上使用可安装的 .exe 文件的用户可以从 [GitHub releases](https://github.com/git-for-windows/git/releases/latest) 下载安装包。

或者，如果你更喜欢在 Windows 上使用包管理器，通过以下命令使用 `winget` 安装：

``` bash
winget install --id Git.Git -e --source winget
```

### 2. 配置 Git

在你安装好 git 之后，需要进行一些配置。Git 需要你的名字和电子邮件地址来记录提交。

你可以通过以下命令向 git 添加你的名字和电子邮件地址：

``` bash
git config --global user.name "你的名字"
git config --global user.email "你的电子邮件地址"
```

这样你就可以帮助其他人知道谁做了哪些更改，以及如何联系他们。不要忘记，如果没有向 git 提供名字和电子邮件，你将无法创建任何提交。

你还可以参考我们（译者注：It's FOSS）的 [Git 命令指南](https://itsfoss.com/basic-git-commands-cheat-sheet/) 来了解其他基本命令。

### 3. 创建 GitHub 或 GitLab 账户

在安装并配置好 Git 之后，我们就可以继续创建 GitHub 或 GitLab 账户了。如果你已经有了账户，请跳到下一步。

要创建 GitHub 账户，请 [点击此处](https://github.com/signup)。如果你想要创建 GitLab 账户，请 [点击此处](https://gitlab.com/users/sign_up)。

提供你的名字、电子邮件地址，选择一个合适的用户名和一个强密码。在你设置好你的账户后，我们强烈建议你也设置双重认证。关于如何在 GitHub 上启用 2FA 的文档可以在 [这里](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication)找到，GitLab 用户应该 [查看这里](https://docs.gitlab.com/ee/user/profile/account/two_factor_authentication.html)。

### 4. 我该如何提交一个 Pull Request？

要参与 Hacktoberfest 2022（原文为 2022，实际应为 2024），你必须有 4 个 Pull Request 被接受/合并。我将演示如何提交一个 Pull Request。

我更偏好使用 GitLab，但 GitHub 在新加入开源社区的人中更受欢迎，所以我将使用 GitHub 演示这个过程。对于 GitLab 用户，步骤是相同的，只有一些用户界面上的差异。

#### a. Fork 一个仓库

「fork 一个仓库」的操作是指创建你自己的仓库副本，以便在其上工作。因此，让我们在 [GitLab](https://gitlab.com/explore/projects/topics/hacktoberfest) 和 [GitHub](https://github.com/topics/hacktoberfest) 上找到一些参与 Hacktoberfest 的仓库来 fork。

我选择了 GitHub 上的 [compress-pdf](https://github.com/itsfoss/compress-pdf) 来做演示。访问你选择的仓库，然后找到「Fork」按钮。

![Deciding a name for your fork of the repository](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/01-fork-800x487.webp)

在你点击「fork」按钮之后，你将被带到一个类似于下面截图的页面。你将被要求给这个仓库起一个名字。最好保持相同的名字，但如果你想修改，也可以这样做。然后，点击「Create fork」按钮。这将创建一个给定仓库的 fork。

![Deciding a name for your fork of the repository](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/02-name-repo.png)

在你 fork 好仓库后，克隆（clone）它。我个人更喜欢通过 SSH 克隆。如果你还没有设置 SSH，你可以参考 GitHub 的 [官方文档](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) 进行设置。

![Cloning the forked repositor](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/03-clone.webp)

在你克隆好仓库之后，你就可以在本地开始工作了。

接下来我将展示如何进行工作，以及如何以 Pull Request 的形式将这些更改发送回「上游」。

#### b. 在本地的 Git 仓库中工作

在你讲仓库克隆到本地后，立即创建一个新分支。使用一个最能描述你将进行的更改的名称。以下命令可以在 git 中创建一个新分支：

``` bash
git checkout -b 分支名称
```

当你使用 `git checkout` 命令和 `-b` 选项时，你将自动切换到这个分支，并可以开始工作。

![Deciding a name for your fork of the repository](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/04-new-branch-800x520.webp)

你可以使用 `git diff` 命令查看你的修改。

![Checking what changes were made; using the 'git diff'](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/05-git-diff.webp)

如果你对你的更改满意了，现在是检查它们是否嫩工作的最佳时机。一旦验证通过，你可以使用 `git add` 命令将这些更改添加到暂存区。

然后，使用 `git commit` 命令创建一个提交，并附上一个有意义的消息。

![The git log command showing the commit I made](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/06-git-log.webp)

#### c. 将代码推送到仓库

现在你已经完成了实现一个东西或者改变现有的某些东西的工作，并提交了它，现在是时候将代码发送回原始仓库了。在这之前，我们的更改需要被提交到我们 fork 的仓库。

要发送我们的更改（这些更改是在一个单独的分支中进行的），请以下面的方式使用 `git push` 命令：

``` bash
git push --set-upstream origin BRANCH-NAME
```

这样你之前创建的分支就会被发送到 fork 的仓库中。

在这个步骤完成后，如果你使用的是 GitHub，你将会看到一个消息，其中会提供一个链接。访问这个链接将为你的分支创建一个 Pull Request。由于这是 GitHub 特有的，我将展示另外一个创建 Pull Request 的方法。

![Pushing your local branch to the GitHub repository](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/07-git-push.webp)

在你的浏览器中，访问你 fork 的仓库。你会看到一个按钮，上面写着「Compare & pull request」。

![Creating a pull request from the GitHub web UI](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/08-cmp-pull-req.png)

点击它将使你跳转到一个要求你填写一个评论的网页。这是你描述诸如「为什么我的提交有用」，「我的提交提供了什么」，「如果合并我的提交会破坏任何现有代码」等内容的地方。

![Drafting a message/comment for your pull request](https://static.fosscope.com/articles_img/2024/10/how-you-can-contribute-to-open-source-in-hacktoberfest/09-send-pr.webp)

在你写好包含所有细节的评论后，点击「**Create pull request**」按钮。恭喜你！

你刚刚提交了你的第一个 Pull Request！

## 这只是你的第一次贡献，希望你能做更多

前几个 Pull Request 总是会让你对刚刚发送的更改感到紧张。不要担心，当你熟悉流程后，这种紧张感会消失。

当一个项目的所有者或维护者有空时，他们会查看你的 Pull Request。如果所有的更改对他们来说没有问题，那么这个 Pull Request 将会被合并。多么令人兴奋！

如果你的 Pull Request 没有被合并，不要担心。**礼貌地**向拒绝你的 Pull Request 的人提出疑问。询问他们问题所在以及如何才能使你的更改被合并。

你是否引入了一个有更优秀的替代品的新库/依赖项？或者，有什么可以被纠正的地方吗？

当然，维护者可能不会回答你的每一个问题。所以，请确保在你发送了关于 Pull Request 的疑问后，不要反复打扰他们。

有一个没被合并的 Pull Request 不会引发世界末日。尝试使用你的激情和创造力参与其他项目，一切都会顺利的！
