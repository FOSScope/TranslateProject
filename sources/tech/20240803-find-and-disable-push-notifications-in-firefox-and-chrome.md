---
title: Find and Disable Push Notifications in Firefox and Chrome
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/disable-push-notifications-chrome-firefox.webp
cover: https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/disable-push-notifications-chrome-firefox.webp
categories:
  - 翻译
  - 技术
tags: 
  - 教程
authorInfo: |
  via: {{via}}

  作者：[Sreenath](https://itsfoss.com/author/sreenath/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
applied: false # 是否已被申领翻译
translated: false # 是否已翻译完成
proofread: false # 是否已校对完成
published: false # 是否已发布
---

Here's how to disable the annoying push notifications in Firefox and Google Chrome.

<!-- more -->

Push notifications in browsers allow websites (if allowed) to display notifications for new activity on your desktop.

When you visit a website that wants you to send notification, you'll a pop-out of this sort:

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/push-notification-displayed-in-firefox-2.webp *Push Notification Permission in Firefox* %}

If you allow, you'll start getting desktop notifications for new activities about that website.

For example, if you are a member of It's FOSS Community forum, you can get desktop notifications when someone replies to your posts.

Many websites also use push notifications to inform you when a new article is published. This happens even when the website is not opened in the browser.

But occasionally, this can be annoying, too 😠 Specially when a website starts sending too many or irrelevant notifications.

In this article, I will explain how to disable push notifications in Firefox and Chrome, two of the most popular web browsers on the internet.

The **process should be similar for other Chromium-based browsers** as well.

## Disable Push Notification in Firefox

Let's see how you can block push notifications for a specific website or multiple of them.

### 1. Disable push notifications for specific websites

While you are browsing that particular site, you can click on the website settings button on the address bar as shown below:

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/revoke-site-notification-permission-in-Firefox-site-settings-button-1.webp *Remove the Notification Permission* %}

This will list the permissions that site has. If it has notification permission allowed, click on the cross icon adjacent to "**Send notification**s" to revoke that permission.

### 2. Disable push notification from multiple websites

There is **another way to disable notifications for multiple websites in one go**.

First, click on the top-right hamburger menu and head to the settings.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/select-settings-in-firefox.png *Select Settings in Firefox* %}

Within the settings menu, go to the **Privacy and Security** tab and scroll down to the **Permissions** section. Here, click on the Settings button adjacent to the Notification item.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/cllick-on-notification-settings-button-firefox.png *Select Notification Settings in Firefox* %}

In the resulting window, you can Allow/Block notification of individual websites, or remove permissions, for all the websites (more on that below).

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/change-individual-site-notification-block-firefox.png *Change Individual Site Notification Settings* %}

Click on **Save Changes** to save the settings.

### 3. Disable push notifications from all sites & block new requests

In that same permission window that you see above, you can also choose to remove all the sites allowed for displaying notifications.

Fret not, if you skipped directly to this method, let me tell you again:

Go to **the Hamburger Menu → Settings → Privacy and Security**. Scroll down to the **Permissions** section and select the Settings button adjacent to “Notifications”.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/cllick-on-notification-settings-button-firefox-1.png *Notification Settings in Firefox* %}

Inside the new window, click on the **Remove All Website** button. This will revoke all the notification permissions.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/remove-all-website-notification-permission-and-disable-further.png *Remove all Notification Permissions* %}

{% note color:cyan 💡 If you want, you can select the**Block new request asking to allow notifications**checkbox. Doing this will prohibit websites from asking for notifications permission in the future. %}

Once changes are made, click on the **Save Changes** button to finish the settings.

## Disable Push Notification in Chrome

The steps applicable for Google Chrome should work on any Chromium-based browser, with slight differences, such as Microsoft Edge offers a “**Cookies and site permissions**” menu and Brave offers "**Site and Shield**" settings.

They all work the same way, only a tad bit different in how the options are accessible to you.

### 1. Disable push notification for single site

If you want to remove the permission of the site you are visiting currently, click on the **permissions** button on the address bar.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/click-on-site-settings-button-in-the-address-bar-to-get-settings.png *Click on Site Settings Button on the Address Bar* %}

From the dropdown menu, disable the permission to send notifications. Either toggle off the *Notifications* option or click on the *Reset Permission* button under Notifications.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/reset-the-notification-permission-of-a-site-in-chrome-browser.png *Reset Site Notification Permission* %}

### 2. Disable notifications for Multiple sites

In Chrome, you can specify a block list with website addresses. And, you won’t receive notifications from these sites.

To do so, like in the previous step, go to **Settings → Privacy and Security → Site Settings → Notifications**.

Now, scroll down to the **Customized Behaviors** section. Here, you can use the **Add** button to add the full addresses of sites, whose notifications you want blocked by default.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/block-selected-sites-to-not-send-notiification.png *Block notifications for selected websites* %}

You can see in the above screenshots, I have blocked several sites from sending notifications.

### 3. Completely disable notification in Chrome

Don’t want any sites to send notifications? You can do that as well.

First, go to **Settings → Privacy and Security → Site Settings → Notifications**.

Under **Default Behavior**, select "*Do not allow sites to send notifications"* button.

{% image https://static.fosscope.com/articles_img/2024/08/find-and-disable-push-notifications-in-firefox-and-chrome/remove-site-notifications-alltogether-in-chrome.png *Do not allow websites to send notifications* %}

That’s it! You won’t receive any website notifications now.

💬*What is your default preference for push notifications on web browsers? Do you find them useful or do you keep them disabled? Let me know your thoughts!*
