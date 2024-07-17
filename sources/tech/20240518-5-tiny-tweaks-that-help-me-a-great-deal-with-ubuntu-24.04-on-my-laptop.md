---
title: 5 Tiny Tweaks That Help Me a Great Deal with Ubuntu 24.04 on My Laptop
date: <发布时间>
author:
  - fosscope-translation-team
  - Betty-hub182
  - <校对者ID>
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/05/ubuntu-laptop-tiny-tweaks.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/05/ubuntu-laptop-tiny-tweaks.png
categories:
  - 翻译
  - 技术
tags:
  - Ubuntu
authorInfo: |-
  via: https://itsfoss.com/ubuntu-tweaks-for-laptop/

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesnied](https://github.com/excniesNIED)
  译者：[Betty-hub182](https://github.com/Betty-hub182)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Some simple tweaks and setting changes I use while running Ubuntu on laptops.

<!-- more -->

Let me share a few tweaks that help me run Ubuntu on my laptops a bit more smoothly.

This is based on my preference, and you may not necessarily make the same changes. Also, these are not ground-breaking, never-seen-before tips.

I am sharing some real simple changes I do while using Ubuntu on my laptops.

And these tips are not specific to Ubuntu 24.04 exclusively. You may find them in other Ubuntu versions as well.

## Enabling tap to click

Traditionally, the touchpad used to have left-click and right-click buttons at the bottom. I believe this was due to the fact that people were more used to of the left and right click buttons on the mouse.

But with time, this behavior changed as users like you and me got more used to just tapping the touchpad for clicking. **One finger tap for left click, two finger tap for right click**.

Laptop manufacturers are aware of this behavior change, and these days, you'll hardly see dedicated left and right-click buttons on the touchpad. Yes, you could still go to the bottom and press it for left and right-click actions.

However, I am more accustomed to the 'tap to click' behavior. I find it more convenient.

This feature can be enabled or disabled from the touchpad settings. Depending on what you prefer.

![Enable Tap to click for laptops on Ubuntu 24.04 ](https://itsfoss.com/content/images/2024/05/tap-to-click-ubuntu-24-04.webp)

{% note color:green 💡 You can also use the 'disable touchpad while typing' feature, which is located at the top of the Touchpad settings. %}

Since you use Ubuntu on a laptop, you should [utilize its three-finger swipe gestures](https://itsfoss.com/three-finger-swipe-gnome/).

{% link https://itsfoss.com/three-finger-swipe-gnome/ %}

## Displaying battery percentage

I prefer keeping an eye on the battery level, be it my smartphone or my laptop.

This way, I don't get the surprise 'low battery' notification.

![Displaying battery percentage on Ubuntu 24.04](https://itsfoss.com/content/images/2024/05/displaying-battery-percentage-ubuntu.png)

You can enable this option from the bottom section of Power settings.

![img](https://itsfoss.com/content/images/2024/05/display-battery-percentage-ubuntu-24-04.webp)

{% note color:green 💡 Did you know you can check the battery level of connected Bluetooth devices? It is displayed in the Power settings but to display it in the top panel, you'll have to use a GNOME Extension [like this one](https://extensions.gnome.org/extension/3991/bluetooth-battery/?ref=itsfoss.com). %}

## Disabling auto-locking due to inactivity

If you leave your Ubuntu laptop unattended, the screen dims and locks the system automatically. And this happens in just 5 minutes of activity.

Now, it could be debatable because it's surely a 'security feature', but I don't like it.

I don't like to enter the password again just because I haven't used my laptop for 5 minutes.

In the **Privacy & Security** settings, there is a dedicated section for Screen Lock.

![Automatic screen lock feature in Ubuntu](https://itsfoss.com/content/images/2024/05/screen-lock-settings-ubuntu-24-04.png)

Here, you can easily disable the automatic screen lock feature.

![Disabling automatic screen lock feature in Ubuntu](https://itsfoss.com/content/images/2024/05/disable-automatic-screenlock-ubuntu.png)

You may also explore other settings for your lock screen such as getting notifications on the lock screen.

{% note color:green 💡 You can press Super (Windows) key + L to to lock the Ubuntu system quickly. %}

## Using different power profiles

In Ubuntu, you get three power modes:

- Performance: High CPU/GPU usage and reduced battery duration
- Balanced: Standard CPU/GPU usage and battery usage
- Power Saver: Focus on conserving battery by reducing CPU/GPU performance

Needless to say when you are not connected to a power source, you would be better off with Balanced and Power Saver mode.

These modes can be accessed by clicking the top right corner and clicking the Power Mode option.

![Power modes in Ubuntu 24.04](https://itsfoss.com/content/images/2024/05/power-profile-ubuntu-24-04.webp)

You can explore more options in the Power settings.

Some people use [tlp](https://linrunner.de/tlp/index.html?ref=itsfoss.com) to extend battery life on Linux. I used to do that several years ago but don't do that lately as I didn't observe any benefits at least on the default settings. It also conflicts with the power profiles.

But if you want to learn more about it, there is a pretty good video by Michael Horn.

{% video youtube:GDdGK8Z_qzs width:100% autoplay:0 %}

My [TUXEDO laptop came with Linux pre-installed by default](https://itsfoss.com/get-linux-laptops/). Since [TUXEDO](https://www.tuxedocomputers.com/index.php?ref=itsfoss.com) is a Linux system manufacturer, they have their own [TUXEDO Control Center app](https://www.tuxedocomputers.com/en/TUXEDO-Control-Center-TCC.tuxedo?ref=itsfoss.com) that lets you change to different power profiles, control CPU fans, create custom profiles and do a lot ofadvanced changes. Note that you CANNOT use it on non-TUXEDO devices.

{% link https://news.itsfoss.com/tuxedo-infinitybook-pro-16-review/ %}

## Getting the display right with fractional scaling

My TUXEDO InfinityBook has a 2K (2560x1600px) screen. While my Dell XPS has a 4K screen.

The icons, fonts and everything else look small on both screens. But if I scale the resolution to 200%, they look too big, especially on the 2K screen.

Thankfully, Ubuntu provides the fractional scaling option. Enable it, and you can scale the display by 25%.

![Using Fractional Scaling on Ubuntu 24.04](https://itsfoss.com/content/images/2024/05/enable-fractional-scaling.png)

This way, I have set 125% on the 2K screen and 150% on the 4K screen.

This is all a matter of personal preference, and I am glad there is an option to set these preferences.

## There are a lot more tweaking you can do

I am restricting this article to laptop-centered tweaks. Otherwise, I usually do many more tweaks on my Ubuntu system. Nightlight, [click to minimize](https://itsfoss.com/click-to-minimize-ubuntu/), and do-not-disturb are just a few that come to my mind at the moment.

Here are a [few more Ubuntu customization tips you can explore](https://itsfoss.com/gnome-tricks-ubuntu/).

{% link https://itsfoss.com/gnome-tricks-ubuntu/ %}

💬 What settings do you change while using Ubuntu or any other Linux distribution on a laptop? Please share it in the comments.
