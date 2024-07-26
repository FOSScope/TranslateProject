---
title: My 30-Day Experiment With Native Linux Games
date: {{release_date}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/linux-gaming-review.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/linux-gaming-review.png
categories:
  - 翻译
  - 新闻
tags: 
  - Linux
  - 游戏
authorInfo: |
  via: https://news.itsfoss.com/native-linux-game-experience/

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Testing supported games on a Linux system from Steam. Here's how it went.

<!-- more -->

Ever since my Windows-equipped gaming PC broke down, not due to Windoze 😆, but due to a blown power supply unit (PSU), I have been gaming on my Ubuntu-equipped laptop for the past few weeks.

Surprisingly, the experience has been [quite good](https://news.itsfoss.com/windows-game-on-linux-experience/), with both non-native and native games running well. Of course, I did run into some issues, but, there have been some great times too!

So, come along as I take you through my experience playing native games on Linux.

## Native Linux Games: More People Should Know About This!

[![an illustration with a penguin and gamepad with a blue green background having a prism pattern](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_a.png)](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_a.png)

For this article, I will be taking a look at three popular native games, that I installed using the official Steam client (*.deb*) for Linux. The test system used has the following specifications:

- **Model:** Dell G15 5530
- **RAM:** 16 GB
- **CPU:** Intel Core i5-13450HX
- **GPU:** NVIDIA GeForce RTX 3050 6 GB
- **Display:** 15.6", FHD 1920×1080, 120Hz & 24" FHD 1920×1080, 60Hz
- **Driver:** NVIDIA 535.183.01
- **OS:** Ubuntu 22.04.4 LTS
- **Power Mode:** Balanced
- **DE:** GNOME 42.9
- **Session:** X11
- **Mods:** No

## Counter-Strike 2

We start things off with the popular [Counter-Strike 2](https://store.steampowered.com/app/730/CounterStrike_2/), which is a successor to the well-known CS:GO. To get constant 120 fps, the maximum supported by my laptop's internal monitor, I had to tweak some graphical settings, mostly between medium or high.

[![a screenshot of counter strike 2 running on ubuntu 22.04.4 lts](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_b.jpg)](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_b.jpg)

I played multiple game modes such as Casual, Deathmatch, Arms Race, Competitive, and my favorite, Premier. In almost all those matches, I was getting a smooth 120 fps experience, with no audio/video issues.

But, there were some other weird issues. Occasionally, the game would just crash, with no error code or anything, one moment the game would be running fine, the other I am staring at my desktop's wallpaper.

Another issue was when I had an external monitor attached. Whenever I tried dragging the game to the faster laptop screen, the game would refuse to maximize, I had to click on the game icon in the dock to get it to come forward.

The same would sometimes happen with just the laptop's monitor active, to resolve the issue, alt-tabbing between apps usually did it for me.

## American Truck Simulator

Another game that I played was [American Truck Simulator](https://store.steampowered.com/app/270880/American_Truck_Simulator/), if you have gone through my periodically updated [best Steam Games on Sale](https://news.itsfoss.com/best-steam-games-linux-sale/) list, you might know that I like playing simulation games.

[![a screenshot of american truck simulator running on ubuntu 22.04.4 lts](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_c.jpg)](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_c.jpg)

Even though its sister game, [Euro Truck Simulator 2](https://store.steampowered.com/app/227300/Euro_Truck_Simulator_2/) is my personal favorite among the two, American Truck Simulator held its own when I played it on Linux.

I did some long-haul trips that took me from the southwest of the USA, to the northwest, and I never faced any crashes, my Peterbilt truck, on the other hand, has seen things. ☠️

The [World of Trucks](https://www.worldoftrucks.com/) integration was working as expected, and I was also able to resume from my old career save.

Even the internet radio was working as expected, allowing me to tune into some real life American radio channels, as I cruised through iconic routes. Sadly, there were some issues with this game too.

The photo you see above, do you notice how washed out and bright it looks?

When I used the in-game photo mode (*which is also bound to Steam's screenshot utility)* that was the result, and to be clear, it was dark and gloomy in the game world due to the rainy weather.

But, it gets even worse. 👇

[![a screenshot of american truck simulator running on ubuntu 22.04.4 lts](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_d.jpg)](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_d.jpg)

The original image was pointed in the wrong direction, and was mirrored, I had to edit it using [Shotwell](https://shotwell-project.org/doc/html/) before adding it to the article. There's also [a report](https://steamcommunity.com/app/270880/discussions/0/4554911223882789939/) by another user on Steam Community facing a similar issue. I truly hope [SCS Software](https://www.scssoft.com/) fixes whatever's causing this.

Another issue that I faced was that I could not use the mouse cursor outside the game window. Even the super key was not working when I was in the game, luckily, I could alt-tab, but without the mouse cursor, I was back to square one.

Do note that the above-mentioned issues occurred both with the internal laptop monitor, and when an external 60Hz display was connected.

## Rail Route

[![a screenshot of rail route running on ubuntu 22.04.4 lts](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_e.jpg)](https://news.itsfoss.com/content/images/2024/07/Native_Linux_Games_e.jpg)

Among the games in this article, [Rail Route](https://store.steampowered.com/app/1124180/Rail_Route/) was by far **the best performer**, it never crashed, never misbehaved when I changed workspaces, or monitors, and window switching was just effortless.

As you can see above, I was able to manage a vast network of both passenger and freight traffic, in the rush-hour game mode. It was fun, yet challenging.

**Suggested Read** 📖

{% link https://news.itsfoss.com/windows-game-on-linux-experience/ Running One of My Favorite Windows Game on Linux: Here’s How It Went icon:https://news.itsfoss.com/content/images/2024/07/cyberpunk-game-ubuntu-review.jpg %}

## My Thoughts

Irrespective of the issues I ran into, I still game on my Linux PC daily, and I am sure that the experience will improve over time, more so if people start gaming on Linux in greater numbers. So, the developers can receive accurate reports to fix what's wrong, which should indirectly help other non-native games.

*💭 What do you think about the Linux gaming experience? What do you play on your Linux system?*

