---
title: 如何使用 Pyenv 在 Ubuntu 上安装多个 Python 版本
date: 2024-07-20 23:12
author:
  - fosscope-translation-team
  - Cubik65536
  - cysnies
banner: https://static.fosscope.com/articles_img/2024/07/pyenv-ubuntu/install-multiple-python-with-pyenv.webp
cover: https://static.fosscope.com/articles_img/2024/07/pyenv-ubuntu/install-multiple-python-with-pyenv.webp
categories:
  - 翻译
  - 技术
tags:
  - Python
  - Ubuntu
  - Pyenv
authorInfo: |
  via: https://itsfoss.com/pyenv-ubuntu/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[Cubik65536](https://github.com/Cubik65536)
  校对：[cysnies](https://github.com/cys2004)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Pyenv 工具可以让你在同一系统上安装和使用不同的 Python 版本。

<!-- more -->

如果你在探索基于 Python 的项目和包，你可能会遇到需要不同 Python 版本的情况。我在尝试 [安装 PyCoral 库](https://coral.ai/docs/accelerator/get-started/?ref=itsfoss.com#2-install-the-pycoral-library) 时就遇到了这种情况，它只能与 Python 版本 3.6 到 3.9 兼容，而我的系统上安装的是 Python 3.11。

好消息是，你不需要卸载系统提供的现有 Python 版本，然后再安装新的 Python 版本。

你可以通过一个叫做 Pyenv 的工具来安装多个 Python 版本。在本教程中，我将向你展示如何在 Ubuntu 和基于 Debian 的发行版上安装和使用这个工具，以便同时获取多个 Python 版本。

## 在 Ubuntu 上安装 pyenv

由于 pyenv 是从源代码构建 Python 的，所以，为了使用 pyenv，你需要安装构建依赖项。

在 Ubuntu 和基于 Debian 的发行版上，你可以使用以下命令来获取所有必要的软件包。

```bash
sudo apt install -y make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python3-openssl
```

你可能已经安装过上述软件包中的一部分了。

当安装好依赖项后，你可以使用 [官方脚本](https://github.com/pyenv/pyenv-installer/blob/master/bin/pyenv-installer) 来安装 pyenv：

```bash
curl https://pyenv.run | bash
```

这个命令会下载脚本并运行它。

当脚本执行完毕后，它会给出一些使 pyenv 能够被自动加载的指引。这个输出取决于你使用的 shell。对于在使用 bash 的我来说，它是这样显示的：

```bash
# Load pyenv automatically by appending
# the following to 
# ~/.bash_profile if it exists, otherwise ~/.profile (for login shells)
# and ~/.bashrc (for interactive shells) :

export PYENV_ROOT="$HOME/.pyenv"
[[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
eval "$(pyenv init -)"
```

所以，我编辑了 `~/.bashrc` 文件，并将上述代码放在文件末尾。

在这之后，你可以重新加载 shell，或者直接重启终端：

```bash
exec "$SHELL"
```

让我们通过检查 pyenv 的版本来验证它是否已经安装在你的系统上：

```bash
pyenv --version
```

如果你看到了一些数字而不是错误，那么 pyenv 就已经在你的 Ubuntu Linux 上安装好了。是时候来看看如何使用它了。

## 使用 pyenv 安装不同的 Python 版本

你可以使用以下命令列出 pyenv 提供的各种 Python 版本和虚拟环境：

```bash
pyenv --list
```

然而，它会显示大量的输出，其中可能包含你不感兴趣的内容。

如果你对各种 Python3 版本感兴趣，可以用正则表达式和 grep 的魔法。例如，如果你对 3.6 到 3.9 之间的 Python 版本感兴趣，可以使用：

```bash
pyenv install --list | grep " 3\.[6789]"
```

这个列表仍然很长，但不像之前看到的那么庞大。

我将通过 PyCoral 库尝试 Coral 项目，而它只能与 Python 3.6 到 Python 3.9 兼容。如果我查看 [Python 版本的状态](https://devguide.python.org/versions)，3.9 看起来是一个不错的选择。我将选择 3.9.19 版本：

```bash
pyenv install -v 3.9.19
```

由于 Python 是从源代码构建的，所以可能需要一些时间，并且会有很多输出。只需要确保其中没有出现错误即可。

## Python 版本的位置

由 pyenv 安装的不同 Python 版本位于 `~/.pyenv/versions/` 目录中。

```bash
abhishek@raspberrypi:~ $ ls ~/.pyenv/versions/
3.9.19
```

## 列出已安装的 Python 版本

你可以使用以下命令查看已安装的其他 Python 版本：

```bash
pyenv versions
```

这个应该显示系统版本（由你的发行版安装的 Python 版本）和 pyenv 安装的其他版本：

```bash
* system (set by /home/abhishek/.pyenv/version)
  3.9.19
```

{% note color:green 💡 上述命令输出中的星号 \* 表示当前激活的 Python 版本。 %}

## 使用其他 Python 版本

如果你只想使用特定的 Python 版本来运行某些东西，你可以这样做：

```bash
pyenv exec python3.9.19 test.py
```

你也可以将默认的 Python 版本更改为你选择的版本：

```bash
pyenv global 3.9.19
```

你可以通过查看版本列表中带有 \* 的条目来确认默认激活的 Python 版本是否已经被更改：

```bash
abhishek@itsfoss:~ $ pyenv global 3.9.19
abhishek@itsfoss:~ $ pyenv versions     
  system
* 3.9.19 (set by /home/abhishek/.pyenv/version)
abhishek@raspberrypi:~ $
```

之后，你可以切换回系统版本：

```bash
pyenv global system
```

## 删除其他 Python 版本

这个也很简单。你可以删除它的文件夹：

```bash
rm -rf ~/.pyenv/versions/<python_version_to_delete>
```

或者，使用以下 pyenv 命令：

```bash
pyenv uninstall <python_version>
```

## 优先使用虚拟环境

即使你安装了多个 Python 版本，最好还是使用虚拟环境。在本教程中，我将向你展示如何在 Ubuntu 和基于 Debian 的发行版上安装和使用这个工具，以便同时获取多个 Python 版本。这样，你就不会在系统级别上搞乱软件包了。

比如，我想要为一个名为 coral 的项目使用 Python 3.9.19。我将会为这个项目创建虚拟环境（虚拟环境的名称和项目名称不需要完全相同）：

```bash
pyenv virtualenv 3.9.19 coral
```

接着，我切换到这个虚拟环境：

```bash
pyenv local coral
```

然后，你可以验证虚拟环境是否正在被使用：

```bash
abhishek@itsfoss:~ $ pyenv which python
/home/abhishek/.pyenv/versions/coral/bin/python
```

记住，你仍然不能使用 `apt install python-package-name`，并期望它会使用虚拟环境中的 Python 版本安装。你需要使用 pip 来实现这一目的：

```bash
pip install python-package-name
```

这个命令将在指定的虚拟环境中使用你指定的 Python 版本安装所需的 Python 包。

*💬 我希望你会喜欢这篇关于在 Ubuntu 上管理不同 Python 版本的教程。虽然我不是 Python 专家，但如果你有任何问题，我会尽力帮助你。*
