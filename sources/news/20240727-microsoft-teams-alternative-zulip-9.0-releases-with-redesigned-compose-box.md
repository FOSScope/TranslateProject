---
title: Microsoft Teams Alternative Zulip 9.0 Releases With Redesigned Compose Box
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/zulip-9-0-release.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/zulip-9-0-release.png
categories:
  - 翻译
  - 新闻
tags: 
  - Zulip
authorInfo: |
  via: https://news.itsfoss.com/zulip-9-0-release

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Zulip 9.0 adds subtle improvements and a better user experience.

<!-- more -->

Those who have used [Zulip](https://zulip.com/) know that it's a very reliable open-source alternative to the proprietary likes of Microsoft Teams and Slack, which doesn't aim to thrive on its user's data.

Designed to be as intuitive as possible, it's meant to be built around making conversations less chaotic and stressful, while also offering flexibility and extensibility to those who need it.

In a recent announcement, the developers have introduced a new release that features a wide range of improvements and upgrades. So, let's check those out.

## 🆕 Zulip 9.0: What's New?

{% image https://news.itsfoss.com/content/images/size/w1000/2024/07/Zulip_9.0_a-1.jpg A screenshot of the Zulip development community's Zulip installation %}

Being a major release, Zulip 9.0 has arrived with **over 5,300 new commits** when compared to 8.0, and **has seen more than 120 people contribute to it**, who improved the code and added new things to it.

As for the key highlights of this release, we start with the **simplified user onboarding experience** that now has things like a new permanently dismissible banner for explaining common operating situations on Zulip.

An example would be a small prompt to direct a user to use the back button on their browser or desktop app to go back to a page when viewing a conversation, with a “*Got it*” button to dismiss it permanently.

![a screenshot of zulip 9.0 user onboarding experience](https://news.itsfoss.com/content/images/2024/07/Zulip_9.0_b.jpg)

Then there is the more obtrusive prompt to introduce users to their inbox when they first log in, with the developers updating the introductory messages to better explain the various elements of Zulip.

They have also brought about some **new integrations** for [Patreon](https://zulip.com/integrations/doc/patreon), [Grafana](https://zulip.com/integrations/doc/grafana), [GitHub](https://zulip.com/integrations/doc/github), and [GitHub Sponsors](https://zulip.com/integrations/doc/githubsponsors).

![a screenshot of zulip 9.0 improved message composing](https://news.itsfoss.com/content/images/2024/07/Zulip_9.0_c.jpg)

Similarly, the **message composing has received many refinements** that see a redesigned compose box being introduced, which brings improved clipboard paste behavior. This has resulted in Zulip preserving formatting for things like links, bold, italics, bulleted lists, and more.

Draft behavior sees a boost as well, with Zulip now automatically showing the most recent draft for the selected conversation.

There's also a new “[*Reactions view*](https://zulip.com/help/emoji-reactions#view-your-messages-with-reactions)” to check how other people have reacted to a message with emoji reactions.

![a screenshot of zulip 9.0 better reading experience](https://news.itsfoss.com/content/images/2024/07/Zulip_9.0_d.jpg)

The **reading experience with Zulip 9.0 is a noticeable upgrade** over previous releases. Now, the fonts are larger and there's better line spacing to make reading text easier on the eyes.

Users can also choose to hide the left and right sidebars for a more focused reading experience. When those are hidden, the keyboard can be [used](https://zulip.com/help/keyboard-shortcuts#navigation) to move around the app.

Fans of the old design can switch to the “[*compact mode*](https://zulip.com/help/font-size)” from the settings menu. The developers have mentioned that they plan to add controls for changing font size and line spacing with the next major release.

![a screenshot of zulip 9.0 improved user management controls](https://news.itsfoss.com/content/images/2024/07/Zulip_9.0_e.jpg)

For admins, **the user management has been enhanced** by the combining of the user settings panel to allow for one-stop management of current users, deactivated users, and invitations.

**Channel administration sees changes** too, with the channel creation process now being more intuitive, and the channel settings showing additional details, including when it was set up.

### Other Changes & Improvements

There are a few other notable updates that you should be aware of:

- A number of new keyboard shortcuts.
- Redesign of all the menus for a clean look.
- The “*Streams*” feature being renamed to “*Channels*”.
- Various enhancements to improve the efficiency of the code.
- Support for Ubuntu 24.04 being added, and Ubuntu 20.04 removed.
- Zulip server now showing previews of uploaded images in the message feed.

The **mobile apps for Zulip are also set to receive a revamp** later this year, for information on that, and the next major Zulip release, you should go through the [release blog](https://blog.zulip.com/2024/07/25/zulip-9-0-released/).

**Suggested Read** 📖

{% link https://itsfoss.com/open-source-slack-alternative/ Ditch Slack With These Open Source Team Chat Tools icon:https://itsfoss.com/content/images/wordpress/2020/02/Open-Source-Team-Communication-Software.jpg %}

## 📥 Download Zulip 9.0

For access to Zulip 9.0, you can sign up for a free organization account on the [official website](https://zulip.com/) to host an instance on Zulip's servers, sign up for one of the [paid plans](https://zulip.com/plans/), or self-host it.

If you go the self-host way, then the [documentation](https://zulip.readthedocs.io/en/stable/production/install.html) is a must-read, with the required packages being available on [GitHub](https://github.com/zulip/zulip/releases/tag/9.0).

<center>{% button "Zulip 9.0 (GitHub)" https://github.com/zulip/zulip/releases/tag/9.0 %}</center>

However, if you simply want to see the 9.0 release in action, then you can visit Zulip's [development community](https://chat.zulip.org/), which is running the release. You can optionally sign up for an account if you want a more comprehensive experience.

**For existing users**, they can follow the official [upgrade guide](https://zulip.readthedocs.io/en/stable/production/upgrade.html) and [upgrade notes](https://zulip.readthedocs.io/en/stable/overview/changelog.html#upgrade-notes-for-9-0) to get their servers up and running with this release.

*💬 Are you looking forward to implementing this on your existing Zulip server instance?*
