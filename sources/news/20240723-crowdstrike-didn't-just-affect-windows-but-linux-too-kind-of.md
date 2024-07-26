---
title: CrowdStrike Didn't Just Affect Windows But Linux Too! (Kind Of)
date: {{release_date}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/crowdstrike-affects-linux-users.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/crowdstrike-affects-linux-users.png
categories:
  - 翻译
  - 新闻
tags: 
  - CrowdStrike
authorInfo: |
  via: https://news.itsfoss.com/crowdstrike-windows-linux/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

CrowdStrike wreaking havoc everywhere!

<!-- more -->

At the end of last week, the IT industry saw a catastrophic event take place thanks to a faulty patch pushed in to Windows by [CrowdStrike](https://www.crowdstrike.com/), a cybersecurity firm based out of Austin, Texas.

Even though, its timing might've been a boon for those looking to get off work early.

Many critical infrastructures such as Airports and Medical facilities had to bear the brunt of it, **raising many important questions** over dependence on such centralized pieces of tech.

Luckily, the issue has since been [addressed](https://www.crowdstrike.com/falcon-content-update-remediation-and-guidance-hub/), but this didn't stop many, including us, from creating some [funny memes](https://x.com/itsfoss2/status/1814314761254838419) on CrowdStrike's plight.

Sadly, Linux was also affected by Crowdstrike weeks before this catastrophic event occurred, which largely went unknown, until now, that is. 🫤

## CrowdStrike's Incompetence: A Heavy Price To Pay For Second-Class Treatment

![a screenshot of a forum post on rocky linux forums outlining an issue with crowdstrike falcon](https://news.itsfoss.com/content/images/2024/07/CrowdStrike_Linux_Booboo_a.png)

Back in May, a Rocky Linux user posted [an issue](https://forums.rockylinux.org/t/crowdstrike-freezing-rockylinux-after-9-4-upgrade/14041) on the forum which reported that upgrading to [Rocky Linux 9.4](https://rockylinux.org/news/rocky-linux-9-4-ga-release) on servers equipped with CrowdStrike's [Falcon platform](https://www.crowdstrike.com/platform/) would result in a system freeze due to a [kernel panic](https://en.wikipedia.org/wiki/Kernel_panic).

**Other users also chimed in**, facing similar issues, and after going around looking for potential fixes, they finally found one in Red Hat's Customer Portal, more on that in a bit.

On [Hacker News](https://news.ycombinator.com/item?id=41005936&), another user suffering from CrowdStrike's incompetence shared that a fleet of production machines running [Debian](https://www.debian.org/) were taken offline when CrowdStrike pushed an incompatible patch for Debian stable.

When they initially contacted support, CrowdStrike took a day to respond, then asked for more proof, beyond what was already provided, they then took some days to acknowledge it.

And, after making them wait for a couple of weeks, they sent a [root cause analysis](https://en.wikipedia.org/wiki/Root_cause_analysis), which mentioned that they didn't support this specific scenario of Debian stable running version N-1, which the user believed was a supported configuration.

### **But, wait, there's more!**

![a screenshot of red hat customer portal article outlining an issue with cloudflare falcon](https://news.itsfoss.com/content/images/2024/07/CrowdStrike_Linux_Booboo_b.png)

In a similar situation, **many Red Hat Enterprise Linux (RHEL) users also faced issues due to Falcon**, for which Red Hat had to issue multiple warnings.

The [first case](https://access.redhat.com/solutions/7068083) (*subscribers-only*) was the one I mentioned earlier for Rocky Linux, in which kernel panic was observed after booting on Linux kernel 5.14.0-410 and later systems due to the *falcon-sensor* process.

The [second case](https://access.redhat.com/solutions/6971903) was a system crash issue on RHEL 6 and 7, where Red Hat offered a workaround, by suggesting users disable Falcon to mitigate the issue, with the other option being to contact CrowdStrike support for assistance.

*By now, we know how prompt CrowdStrike's customer service is.* ☠️

Unsurprisingly, thanks to all the chaos, the U.S. House of Representatives [Homeland Security Committee](https://homeland.house.gov/) has officially sent a letter to [George Kurtz](https://www.linkedin.com/in/georgekurtz), CEO of CrowdStrike, asking him to testify on the massive outage.

I would have liked to think that this was due to Linux-based OSes being affected, but, as we all know, [Windows](https://www.microsoft.com/en-us/windows/) is the favorite child among all the operating systems for a bulk of the population.

Fun (*or ominous!?*) fact, George was the Chief Technology Officer (CTO) of McAfee back in 2010, when the infamous [DAT 5958](https://en.wikipedia.org/wiki/McAfee#DAT_5958_update) antivirus update managed to cripple millions of Windows-equipped computers around the world.

*💬 The motorsport fan in me knows CrowdStrike from the sponsorship and infrastructure support they do for the Mercedes-AMG PETRONAS* [*F1 Team*](https://www.mercedesamgf1.com/)*. What about you? Did you know of them before?*
