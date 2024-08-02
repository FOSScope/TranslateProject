---
title: Open External Links in AppImage for Login
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/open-external-links-in-appimage.png
cover: https://itsfoss.com/content/images/size/w600/format/webp/2024/07/open-external-links-in-appimage.png
categories:
  - 翻译
  - 技术
tags: 
  - 排除故障
  - AppImage
authorInfo: |
  via: https://itsfoss.com/appimage-open-external-links/

  作者：[Sreenath](https://itsfoss.com/author/sreenath/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

Having trouble logging in with AppImage application? Here's what you can do.

<!-- more -->

AppImage is a popular packaging format for Linux systems. You'll often find applications packaged in this format.

Sometimes, when you try to log in to a service’s AppImage through a browser, even though it will report a success and tell you to go back to the app, it actually won’t.

Let me share a quick tip on how to force open external links in AppImage so that you can log into it through a browser.

## Make AppImage open external links

Here, I am using an AppImage for [Todoist](https://todoist.com/) that needs you to log in through the browser.

First, open the app and click on login through the browser button.

{% image https://itsfoss.com/content/images/2023/10/1-click-on-login-via-browser.png *Click on Login via browser* %}

When it asks you to login, enter the credentials and log in.

{% note color:green 💡 Use Firefox, as that will provide more options for opening external links. %}

{% image https://itsfoss.com/content/images/2023/10/2-click-on-login-button.png *Login through Web Browser* %}

Once you successfully log in, it will ask you to open the app in an external app.

{% image https://itsfoss.com/content/images/2023/10/3-click-on-chose-different-application.png *Choose a different Application* %}

If your System Handler finds the proper app, then there is no issue. If you want to open it in another app of your choice, click on “Choose a different application” link.

Now, click on “Choose” button.

{% image https://itsfoss.com/content/images/2023/10/4-click-on-chose-to-open-file-browser-1.png *Click on Choose* %}

This will bring you to the file chooser. Select the AppImage of your choice, in this case, Todoist, to open that particular link.

{% image https://itsfoss.com/content/images/2023/10/5-select-appimage.png *Locate the AppImage* %}

Click on Select. Once selected, press “Open Link” to open it in the AppImage.

{% image https://itsfoss.com/content/images/2023/10/6-open-link-1.png *Click on Open Link button* %}

That's it. You can see the AppImage will be now logged in.

Please note that this is a very specific scenario and you'll encounter it with very few applications.

I hope this quick tip helps you. Please let me know if you have questions or suggestions in the comments.
