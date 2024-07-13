---
title: Fixing Applications Icon Missing from the Launcher in Ubuntu
date: <发布时间>
author:
  - fosscope-translation-team
  - <译者ID>
  - <校对者ID>
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/06/fix-missing-app-icon-ubuntu.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/06/fix-missing-app-icon-ubuntu.png
categories:
  - 翻译
  - 技术
tags:
  - Ubuntu
  - Troubleshoot
authorInfo: |
  via: https://itsfoss.com/ubuntu-app-icon-missing

  作者：[Abhishek Prakash](https://itsfoss.com/author/abhishek/)
  选题：[excniesnied](https://github.com/excniesNIED)
  译者：[<译者ID>](https://github.com/<译者ID>)
  校对：[<校对者ID>](https://github.com/<校对者ID>)

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Some applications are not displaying their icons in the launcher in Ubuntu? Here's what you can do about it.

<!-- more -->

Recently I encountered a strange issue in Ubuntu 24.04.

When I ran some applications, their icons didn't show in the launcher. Instead, it displayed a gear/settings symbol.

{% image https://itsfoss.com/content/images/2024/06/missing-icons-from-launcher-ubuntu.webp *Some application icons are not shown in the launcher* %}

This was particularly weird because those applications did have icons and the thumbnails were very well displayed in the activity area.

{% image https://itsfoss.com/content/images/2024/06/applications-icons-displayed-in-gnome-activity-menu.webp *But the application icons are properly displayed in GNOME Activity*  %}

Even more surprising was that it happened with the Transmission torrent client that comes preinstalled with Ubuntu.

In this tutorial, I'll share how I fixed this missing icon issue. But before that, let me discuss what was wrong here.

{% note color:red 🚧 This tutorial is only valid for the GNOME desktop environment. %}

## The missing element mystery

Alright! Here's the thing. Every application you install should have a .desktop file that has various information, including the location of the application icon.

This .desktop file is essential for the desktop integration. Without it, you won't be able to search for the installed application in the menu, the thumbnail and icons won't be displayed.

But in my case, both ONLYOFFICE and Transmission had their desktop files in the `/usr/share/applications` directory. I even made sure that the icon image file was present.

It baffled me and I started going through GitHub and forum discussions. This is when I came across [this discussion about missing WM_CLASS property](https://askubuntu.com/questions/1251172/active-application-icon-not-shown-on-dock?ref=itsfoss.com) in some KDE applications that caused this issue.

The applications I was using were not from KDE but this was a step in the right direction. [This blog post](https://ubuntuhandbook.org/index.php/2024/04/missing-icon-dock-ubuntu-2404/?ref=itsfoss.com) confirmed my views.

{% note color:cyan **📋TLDR** You need to get the WM_CLASS property and update the .desktop file of the application with this value. %}

## Fixing the missing application icons from the launcher issue

{% note color:cyan ✋ While I am trying to go in every step in detail, it still involves some effort on your end. This is not run-this-command to fix the issue kind of solution. You have to take my examples as a reference and use them in your scenario. Basic knowledge of the Linux command line is required. %}

### Step 0: Run the applications in question

You'll have to run the applications that have missing icons. It is essential.

### Step 1: Get the WM_CLASS property of the application

All this is a tad bit easier if you are using Xorg instead of Wayland. Run `xprop WM_CLASS` command in terminal, the cursor becomes crosshair and you click on the desired application to get its WM_CLASS property.

But that is not happening here in Wayland, so let's take the longer route.

Press Alt + F2 to launch “Run a Command” dialog. Your keyboard should have a F2 function key. Look for it. Sometimes they need to run in Fn+2 way. I let you discover that.

Pressing Alt + F2 launches a dialogue box. Enter `lg` (lowercase LG) here:

![ENtering debug mode in GNOME](https://itsfoss.com/content/images/2024/06/bring-debug-mode-gnome.webp)

It will bring up GNOME’s integrated debugger and inspector tool. Your mouse and keyboard has limited function at this stage. Here, click on the Window option and it will show the WM_CLASS property for each running application Window.

{% image https://itsfoss.com/content/images/2024/06/get-wm-class-property-gnome.webp *Click to expand if not visible properly*  %}

Note that copy-paste didn't work for me at this stage. I took a screenshot for reference.

Press Esc to close the debugger.

### Step 2: Edit .desktop file

{% note color:cyan 📋 If you don't have much experience editing config files such as these, make a backup copy of the .desktop file before modifying it. %}

The next step is to edit the application's .desktop file. You should find it in the `/usr/share/applications` directory. If it's not there, you may try looking for it in `~/.local/share/applications` and `/var/lib/flatpak/exports/share/applications/` locations as well.

Now, you can use Nano to edit files in the terminal. This is the example for me:

```
sudo nano /usr/share/applications/onlyoffice-desktopeditors.desktop
```

**But if you are uncomfortable with that, you can also do it graphically**. Just go to the location of your application's .desktop file.

In the file manager, You can click Other Locations and then Ubuntu to access the root directory.

![Accessing root directory in Ubuntu](https://itsfoss.com/content/images/2024/06/access-root-directory-ubuntu.webp)

From there, you can go to the user->share->applications folder. You could also just enter /usr/share/applications in the address bar of the file manager and access it quickly.

In here, **under the [Desktop Entry] section**, add a line

```
StartupWMClass=Value-you-got-in-previous-step
```

![Editing desktop file](https://itsfoss.com/content/images/2024/06/editing-deskto-file.webp)

Save the file. You'll have to enter your account password to save the file.

And the effect is almost immediate. No need to reboot or even log out. The icons get displayed in the launcher almost as soon as you save the file.

![Missing application icon fixed in Ubuntu](https://itsfoss.com/content/images/2024/06/missing-application-icon-fixed-ubuntu.webp)

I experienced that you have limited mouse and keyboard control at this time. The WM Class text could not be copied. So, I took a screenshot and used that screenshot as a reference to see the value and manually type it in.

## Conclusion

It's good to get the missing icons back. It took some effort, but it taught me a few new things in the process. That's what I like about troubleshooting. It teaches you stuff that you would have never known otherwise.

Not sure if I should blame Ubuntu or GNOME. But this is a poor user experience specially when you encounter it with applications that are installed by default.

🗨️ I hope the tutorial is not overly complicated. Did it help you fix the missing icons problem in Ubuntu?
