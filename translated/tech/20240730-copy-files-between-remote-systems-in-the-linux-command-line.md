---
title: 使用 Linux 命令行远程复制文件
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - excniesnied
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/transfer-files-between-cli-and-remote-systems.webp
cover: https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/transfer-files-between-cli-and-remote-systems.webp
categories:
  - 翻译
  - 技术
tags: 
  - 终端
authorInfo: |
  via: https://itsfoss.com/ssh-copy-remote-local/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[Churnie HXCN](https://github.com/excniesNIED)
  译者：[Churnie HXCN](https://github.com/excniesNIED)
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

下面是几种通过 SSH 在远程系统和本地机器之间传输文件的方法。

<!-- more -->

情况是这样的。 您可以通过 SSH 连接到一个远程 Linux 系统，然后您会发现自己需要将一些文件从远程服务器复制到本地系统。

怎么做？ 您可以使用老式的 `scp `命令如下：

```Bash
scp remote_username@remote_server_IP:/dir/location/filename local_dir_path
```

如果要将某些文件从本地系统复制到远程系统：

```Bash
scp local_dir_path/filename remote_username@remote_server_IP:/dir/location 
```

**注意，在远程服务器详细信息和路径之间要用冒号（:）分隔。**

您也可以在这里使用 `rsync` 命令。 让我在本教程中详细介绍这些步骤。

{% note color:yellow ✋ 本教程假定您可以使用 SSH 连接到远程系统。 您需要知道远程用户的密码，并且远程用户应具有对要复制文件的文件夹的读/写访问权限。  %}

我的环境设置包括一个用作远程服务器的树莓派。 我可以通过 TUXEDO 笔记本电脑 [以 SSH 方式](https://itsfoss.com/ssh-into-raspberry/) 轻松连接到 Pi。

## scp 命令的使用

[`scp` 命令](https://itsfoss.com/scp-command/) 是安全拷贝（secure copy）的简称，它使用 SSH 连接在远程系统之间传输文件。 我喜欢它，因为它的语法与 [`cp` 命令](https://itsfoss.com/cp-command/) 相似。

{% note color:green 💡 我打开了一个单独的终端会话，通过 SSH 连接到远程服务器。 这样我就能查看和复制远程服务器上的文件位置。 这一点很重要，因为通过 `SCP` 无法获得制表符完成（文件名或目录名的自动填充）。 %}

### 将文件从本地计算机复制到远程服务器

我在 `Documents` 目录中有一个 `sample.txt` 文件。 我想把这个文件发送到远程服务器的 `Template` 目录中。

您还记得语法吗？

```Bash
scp local_dir_path/filename remote_username@remote_server_IP:/dir/location 
```

它会要求输入密码，即远程服务器上用户的密码。

让我们在这个例子中使用它：

```Bash
scp Documents/sample.txt abhishek@192.168.1.5:~/Templates
```

以下是该命令的输出结果：

![scp copy files from local to remote over SSH](https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/scp-copy-files-from-local-to-remote-system.webp)

我使用 `~` 符号表示用户的主目录，因为它比 `/home/username` 短。

您可以通过 SSH 连接到远程服务器验证传输结果。 这也是我一直单独打开终端会话的原因。

![Verify copying of files from local to remote system](https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/verify-local-to-remote-copy.webp)

**复制多个文件**

使用方法与 `cp` 命令相同：

```Bash
scp file1 file2 fileN remote_username@remote_server_IP:/dir/location 
```

**将文件夹复制到远程系统**

像 `cp` 命令一样，使用递归选项 `-r`：

```Bash
scp -r Dir1 remote_username@remote_server_IP:/dir/location 
```

### 将文件从远程服务器复制到本地计算机

现在让我们反过来。 让我们把远程服务器上的文件复制到本地机器上。 语法如下

```Bash
scp remote_username@remote_server_IP:/dir/location/filename local_dir_path
```

比方说，我在树莓派上有一些截图，我想把它们放到我的笔记本电脑上。

```Bash
scp abhishek@192.168.1.5:~/Pictures/sd-card-copy.png .
```

我将远程文件复制到了当前工作目录。

![scp copy remote file to local](https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/scp-copy-remote-file-to-local.webp)

**复制多个文件？**

复制多个文件意味着要提供所有文件的完整路径（包括用户名和 IP 地址），这就变得很棘手。 如果可以使用通配符匹配，请使用通配符匹配，否则，请将所需文件复制到一个新的临时目录中，然后将该临时目录复制到本地系统。

```Bash
scp -r remote_username@remote_server_IP:/dir_location local_dir_path
```

## rsync 命令的使用

`rsync` 是另一个功能强大的命令，能让您在远程系统之间复制文件。 与 `scp` 不同，`rsync` 不仅仅是一个简单的传输命令，它还有更强大的功能，与 cron 作业结合使用时，它将成为一个很好的备份工具。

在这里，我只向您展示如何使用它进行简单的文件传输。

### 将文件/目录从本地复制到远程位置

要将文件从本地系统复制到远程服务器，可以使用 `rsync `命令：

```Bash
rsync local_file_path remote_username@remote_server_IP:/dir/location 
```

举个例子，我想把本地目录 `NewDir` 复制到远程树莓派的 `Documents` 目录：

```Bash
rsync -r Documents/NewDir abhishek@192.168.1.5:~/Documents
```

![img](https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/rsync-copy-local-to-remote.webp)

### 将文件/目录从远程复制到本地

要将远程计算机上的文件或目录复制到本地计算机上，可按这种方式使用 `rsync`：

```Bash
rsync remote_username@remote_server_IP:/file_location local_dir_path
```

比方说，我想把 `rpdiags.txt` 从远程系统的主目录复制到本地系统的当前工作目录：

```Bash
rsync abhishek@192.168.1.5:~/rpdiags.txt .
```

![use rsync to copy files from remote to local](https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/rsync-copy-from-remote-to-local.webp)

## 结论

如果已配置 SFTP 服务器，则可使用 [FileZilla](https://filezilla-project.org/) 等图形用户界面工具。

{% link https://itsfoss.com/filezilla-ubuntu/ 在 Ubuntu 上安装并使用 FileZilla 连接 SFTP 服务器 icon:https://static.fosscope.com/articles_img/2024/08/copy-files-between-remote-systems-in-the-linux-command-line/install-filezilla-on-ubuntu.webp %}

我更喜欢使用 scp 命令通过 SSH 连接快速传输文件。 当我需要对包含大量文件的文件夹进行备份时，我会使用 rsync。 更多信息请见其他文章。 祝您愉快😄