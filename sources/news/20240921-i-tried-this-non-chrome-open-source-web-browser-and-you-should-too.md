---
title: I tried this non-Chrome Open-Source Web Browser (And You Should Too!)
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
  via: https://news.itsfoss.com/zen-browser/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[Cubik65536](https://github.com/Cubik65536)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

<!-- 所有以 `{{variable}}` 形式展现的内容都需要替换为实际内容 -->

It's time we got to try an open-source browser not based on Chrome. Zen Browser is the hero we didn't know we needed.

<!-- more -->

A few weeks ago, when I was scrolling through our social media handles, many of our followers mentioned a new browser that we should check out called “**Zen Browser**”.

I wondered, is it just another Firefox fork with some technical changes? 🗯️

Because, that's not what we need right now. There are plenty of Firefox and Chrome-based browsers. Beyond that, there's the lesser-known but [unique choices](https://itsfoss.com/unique-web-browsers/) like [Floorp](https://news.itsfoss.com/floorp-firefox/) and [Thorium](https://news.itsfoss.com/thorium/).

**Most of them aren't that interesting in terms of user experience**. But, when I looked at Zen Browser, it definitely caught my attention! 😎

As it turns out, it is **an open-source, cross-platform web browser** **based on Firefox, taking a different approach to the user interface**.

And, I knew, I needed to try it out! So, join me as I take you through my experience.

🚧

Zen Browser is currently under development, and might act out from time-to-time.

![a screenshot of zen browser](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_a.png)

Built on the most recent Firefox release, Zen Browser is written using CSS, C++, JavaScript, and a few other programming languages, with a community of over 30 people contributing to it.

Some **key features** of this tranquil browser include:

I used the latest Alpha version of Zen Browser on my [Fedora 40](https://news.itsfoss.com/fedora-40-release/) laptop to see how it fared. The official *AppImage* ran without a fuss, and at first launch, I was shown **a welcome wizard**.

![a screenshot of zen browser welcome wizard](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_b.jpg)

The welcome wizard took me through the usual first-time setup, allowing me to tweak the appearance, import data from an existing browser, and select a default search engine (*I went for DuckDuckGo*).

![](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_c.jpg)

![](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_d.jpg)

After I was done configuring, Zen Browser's welcome webpage opened up. That is when I noticed that there was **no tab bar at the top or bottom of the browser; rather, it displayed tabs in the side panel**, with the [favicon](https://en.wikipedia.org/wiki/Favicon) of the website being the identifier of a tab.

When I took a look at the address bar, I noticed that [Enhanced Tracking Protection](https://support.mozilla.org/en-US/kb/enhanced-tracking-protection-firefox-desktop) was enabled by default, which is similar to what Firefox does, and I liked that.

![a screenshot of zen browser with the duckduckgo ai chat website open](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_e.png)

The **layout of the interface felt quite clean** to me; there were handy buttons on the top to control the webpage, manage extensions, and a menu with additional options.

There was nothing at the bottom of the interface, but there was **a functional side panel** on the left-hand side of the interface. It featured a workspace switcher button at the very top, with currently open tabs in the middle, and some useful buttons at the lower part.

One of those was a button to access the account that opens up controls for the [profile manager](https://support.mozilla.org/en-US/kb/profile-manager-create-remove-switch-firefox-profiles). The other buttons can be used to expand the side panel, open a sidebar, access bookmarks, browse through the history, and access the settings page.

It was interesting to see that the downloads button was at the top. It would've been more accessible if it was part of the side panel. Just my opinion.

But, that's enough about buttons, let's check out **two of the most impressive features** of Zen Browser:

The **split-view functionality** allows you to open up two different tabs on the same screen, allowing for easy multitasking when working across different webpages.

Here's how it looks:

![a screenshot of zen browser split view functionality in action](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_f.png)

Using it is very straightforward; just select any tabs by using “*Ctrl + Left-Click*”, then right-click on any tab and choose “*Split X Tabs*”, where X is the number of tabs selected.

As you can see above, I split two tabs, but in my testing, **I could split over 10+ tabs** 🤯

Of course, the tab sizes were too small for me to read on my 24-inch monitor. If you have a larger monitor, then you are in for a treat.

Similarly, the second is the **Zen Sidebar** feature, which can run web apps alongside any open tabs. This can be helpful in situations where you need to quickly access a service like a note-taking app, Wikipedia, Telegram, and others.

![a screenshot of zen browser sidebar app functionality in action](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_g.png)

On the **customization side of things**, you will find that Zen Browser supports everything that Firefox does, be it the settings, adding new extensions/themes/plugins, etc. So, you won't have to learn anything new if you are an existing Firefox user.

![a screenshot of zen browser themes setting page](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_h.png)

However, there is a dedicated [Themes Store](https://zen-browser.app/themes), that lists themes built specifically for Zen Browser. It can be quickly accessed from the “*Theme Store*” tab in the settings menu.

I downloaded a theme called “[Solarized](https://zen-browser.app/themes/56449583-f295-4f34-baf8-da70d3d156e7)”, and it came out looking really nice. See for yourself. 👇

![a screenshot of zen browser themes store with the solarized theme page open](https://news.itsfoss.com/content/images/size/w1000/2024/09/Zen_Browser_i.png)

Interestingly, the Themes Store is not only for themes, but also features many other user interface enhancements.

In the end, **I liked the overall experience with the browser**.

&gt; I think Zen Browser is a breath of fresh air in the browser space, despite being a Firefox-based browser.

Sure, there are a few things that could be better, like an easier way to unsplit tabs and a faster way to close them.

The right-click menu just doesn't cut it, and expanding the side panel to close tabs is also not that intuitive. But, it's alright. Development is still in its early stages.

So far, so good!

I also believe it could give a good competition to options like Vivaldi, which is my favorite for its tab management capabilities.

You can get Zen Browser for **Linux**, **Windows**, and **macOS** from the [official website](https://zen-browser.app/download). They also offer it on the [Flathub store](https://flathub.org/apps/io.github.zen_browser.zen) for further accessibility on Linux.

[Zen Browser (Flathub)](https://flathub.org/apps/io.github.zen_browser.zen)

The source code for the desktop applications is hosted on [GitHub](https://github.com/zen-browser/desktop), where you will also find the relevant documentation and ways to contribute to the browser and the project as a whole.

*💬 Do you like the approach Zen Browser is taking in terms of tab management? Let me know below!*
