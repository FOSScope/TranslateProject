---
title: 开放源代码和可获取源代码，二者有何区别？
date: 2024-07-20 23:27:27
abbrlink: 3bcd542b
author:
  - fosscope-translation-team
  - RobertCheng-956
  - Cubik65536
banner: https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/open-source-source-available.webp
cover: https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/open-source-source-available.webp
categories:
  - 翻译
  - 新闻
tags:
  - Open Source
  - License
authorInfo: |
  via: https://news.itsfoss.com/open-source-source-available

  作者：[Ankush Das](https://news.itsfoss.com/author/ankush/)
  选题：[excniesnied](https://github.com/excniesNIED)
  译者：[RobertCheng-956](https://github.com/RobertCheng-956)
  校对：[Cubik65536](https://github.com/Cubik65536)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

对二者感到疑惑？这篇文章将有助于您理解开放源代码（即「开源」）与可获取源代码之间的区别。

<!-- more -->

当提到软件中的术语的时候，总会有事实，也会有观点。

即使你有理由使用某个术语，但有些人可能会对此提出异议。在某些情况下，你可能并未使用该术语来描述某个软件，但其他人却认为你应该这么做。

总而言之，术语的应用情境各有对错，但也常有处于模糊不清的灰色地带的情况。

这就是你涉及到「**开源**」和「**可获取源代码**」软件时的感受。

## 令人困惑但至关重要...

乍一看，这两个术语都在描述可公开访问源代码的软件，对吧？

所以，有些人甚至认为开源和可获取源代码是一样的，都指可以访问或查看软件的代码。

但有趣的地方就在这儿。

虽然这两个术语都肯定了任何软件的透明度，**可获取源代码却是开源的一个子集。**

![source available illustration](https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/source-available.webp)

**可获取源代码**：指的是无论软件使用哪种许可证，无论软件的修改或再分发的权限怎么样，源代码都是公开可访问和可获取的。

例如 **CC BY-NC-SA 4.0 (创作共用署名-非商业性使用-相同方式共享 4.0)** 这类限制商业使用的许可证，被视为使得软件的源代码可以被公开获取。

![open source illustration with the OSI logo](https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/open-source.webp)

**开源**：这意味着整个软件的源代码完全透明，可供公众检视，可以自由分叉进行修改，并能以任意形式重新分发。它也赋予你进行商业利用的权利。符合真正开源精神的许可证，必须获得 [OSI（开源倡议组织）的认证](https://opensource.org/licenses)。

**MIT、GPL-3.0 和 Apache 2.0** 都是开源许可证的例子。

## 那么，为什么会同时存在这两类证书呢？

您可能想知道，如果开源的软件更简单或更优质，为什么还会有可获取源代码的软件呢？

简而言之，**从商业角度来看，这对于一些开发人员和公司来说是必要的。**

![source available money](https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/source-available-money.webp)

例如，心怀叵测之人能够轻而易举地重新分发嵌入了恶意代码的开源软件。当然，除非有人仔细审查，否则用户根本无从得知其中的猫腻。

即便该软件本身并不含任何恶意程序，**这也将对原始软件的可靠性造成打击**。

既然他们是以与开源兼容的许可方式发布软件，他们便无权移除任何包含恶意代码的分叉版本，也无法阻止他人进行此类尝试。

的确，开源许可证赋予了使用者极大的自由，但与此同时，这也可能导致一些负面后果，正如前文所述。

在某些情形下，软件可能会被修改或优化，继而被投入商业市场。有人或许会提出，具备改进软件的能力本身并无不妥，然而，这却可能对原始软件所依托的商业模式构成冲击。（译者注：原句不完整）

相反，若软件采用了与开源倡议不相容的许可协议，开发者或公司则有权移除恶意的衍生版本，并有权禁止那些他们不认同的再分发行为。

可获取源代码的许可证同样限定了软件的商业利用范畴。这样一来，开发人员或是公司就能保证自己的劳动成果不会被他人不当牟利，同时他们自己则可以随心所欲地将其用于个人用途。

## 哪种更好？开源还是可获取源代码？

**二者不存在孰优孰劣**。实际上，这完全取决于开发者和选择使用带有任意相关许可的软件的用户的观点。

有些人可能认为，背离纯粹开源精神的任何事物都是不道德的。而另一些人可能并不介意使用可获取源代码的软件。

就我个人而言，我能够理解双方的立场。我认为，全面考量每件事的利弊才是明智之举。毕竟，没有任何东西是完美无缺的，每个选项都存在瑕疵。

✅ **我相信，与专有软件相比，这两种许可证都推动了软件代码的透明度。**

因此，我们应当支持那些依据自身愿景或规划，选择采用这些许可证来开发软件的项目。

## 可获取源代码产品示例

![anytype source available](https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/anytype.webp)

近期的一个源码公开产品例子就是 [Anytype](https://anytype.io/)，一款主打本地优先和隐私保护的 Notion 替代应用。

您可以查看其源代码，并了解其核心。但是，您你不能将代码用于任何形式的商业活动，仅限于个人使用。

他们选择了定制的许可证「**Any Source Available License 1.0**」，以此防止他人利用他们的创造牟利，这种做法是为了保护他们的商业利益不受侵害。有的时候，某些产品会选择 [**CC BY-NC-SA 4.0** 许可证](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.en) 这样的许可证，比如现在已经不再运营的 Skiff Mail 邮件服务。

确实，有人批评在营销材料中将「**开源**」这一术语应用于这类产品和服务是不当的。的确，这样的描述不够精确。而 Anytype 采取的做法则是简单地使用「Open」这个词，并明确指出它是可获取源代码的。

![anytype website screenshot showing open code](https://static.fosscope.com/articles_img/2024/07/from-open-source-to-source-available-how-things-changed/anytype-open.webp)

所以，他们并未故意误导，但我们确实需要明辨这两者间的差异，毕竟在同一页面上他们也有一个「开源」标识的视频。

不要忘了，怀旧风的媒体播放器 Winamp 也在采取类似的策略：

{% link https://news.itsfoss.com/winamp-open-source/ %}

我们唯有等到他们公开其代码仓库的那一天，才能确切分辨出这款软件是真开源还是仅限可获取源代码。

我猜想，或许正因为不是每位网络用户都能即刻领悟「可获取源代码」的内涵，这才导致了一些产品最终倾向于用「开源」这个词汇来描述自身。

*💬 您对于两者之间的差异有何看法？如果您要做出选择，您会偏向哪一方，原因何在？欢迎在下方留言区分享您的见解！*
