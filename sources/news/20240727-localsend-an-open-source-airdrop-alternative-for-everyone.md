---
title: LocalSend: An Open-Source AirDrop Alternative For Everyone!
date: {{release_date}}
abbrlink: {{abbrlink}}
author:
  - fosscope-translation-team
  - {{translator}}
  - {{proofreader}}
banner: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/Localsend.png
cover: https://news.itsfoss.com/content/images/size/w1304/format/webp/2024/07/Localsend.png
categories:
  - 翻译
  - 新闻
tags:
  - AirDrop
authorInfo: |
  via: https://news.itsfoss.com/localsend

  作者：[Sourav Rudra](https://news.itsfoss.com/author/sourav/)
  选题：[excniesNIED](https://github.com/excniesNIED)
  译者：[{{translator}}](https://github.com/{{translator}})
  校对：[{{proofreader}}](https://github.com/{{proofreader}})

  本文由 [FOSScope翻译组](https://github.com/FOSScope/TranslateProject) 原创编译，[开源观察](https://fosscope.com/) 荣誉推出
---

It's time to ditch platform-specific solutions like AirDrop!

<!-- more -->

If you are an Apple user, then you have most likely used [AirDrop](https://support.apple.com/en-us/119857) to wirelessly transfer files to other Apple devices.

Similarly, for Android, there's [Quick Share](https://support.google.com/android/answer/9286773?hl=en&) (formerly known as Nearby Share) that does the job perfectly. For Linux, there's an app called [Warp](https://news.itsfoss.com/warp-file-sharing/) that does the same, but between Linux and Windows only.

And, if you want to transfer between your Android and Windows device, you will have to try the Windows Phone Link app.

It is subjective to what your use-case is, and what you find more intuitive. But, what if I said that there's an open-source app that can do file transfers, but across all the above-mentioned devices? 🤔

With this [First Look](https://news.itsfoss.com/tag/first-look/), we will be taking a look at an **open-source** **file transfer app** called “**LocalSend**”, which allows you to securely share files and messages across devices.

## LocalSend: Overview ⭐

![a screenshot of localsend](https://news.itsfoss.com/content/images/2024/07/LocalSend_a.png)

LocalSend is **a cross-platform file transfer app** that's freely available under the [MIT License](https://opensource.org/license/mit), and is maintained actively by various contributors. It is primarily written in the [Dart](https://dart.dev/) programming language.

Some **key features** include:

- **Offline Sharing**
- **No Account Creation**
- **End-to-end Encryption**

### Initial Impressions 👨‍💻

For testing this out, I disconnected the modem from my Wi-Fi router, but this should also work well with internet access, and even for wired networks in a home or office setting.

Do note that the sending/receiving speeds will depend on your router and/or Ethernet cables.

First, I checked out how **file transfers between Linux and Android** worked.

On my Ubuntu 22.04.4-equipped laptop, I installed the official flatpak, and similarly, the official app for my Android 14-equipped Samsung smartphone.

![a screenshot of localsend with some files selected for sending and a nearby device being shown](https://news.itsfoss.com/content/images/2024/07/LocalSend_b.png)

After selecting a few images, documents, and audio files by going into the “*Send*” page, I initiated transfer to my Android device (*Determined Pineapple*), for which approval was required on the phone's app to start receiving files.

![a screenshot of localsend waiting for response from an android device it is sending files to](https://news.itsfoss.com/content/images/2024/07/LocalSend_c.png)

As you can see below, the Android app asked me whether I wanted to accept or reject the files being sent by “*Big Banana*”, the name of my Ubuntu device on the LocalSend app.

{% image [https://news.itsfoss.com/content/images/size/w1000/2024/07/local-send-android-screenhots.jpg](https://s.xaox.cc/xaoxuu/posts/202401131914137.jpg-hd) Receiving files from Ubuntu on Android using LocalSend %}

Before I accepted, I went into the “*Options*” menu to review what files I was about to receive, I had the chance to select specific files, and even rename them before the upload started.

During the transfer, a handy progress bar showed up, with options to enable “*Advanced*” that would show me detailed metrics like transfer speed, and another option to “*Cancel*” the transfer.

![a screenshot of localsend after sending of files is complete](https://news.itsfoss.com/content/images/2024/07/LocalSend_h.png)

After the file transfer was done, I was shown a “*Finished*” prompt on both the apps, and I must say, **the transfer speeds were superb**.

I then checked out how **file transfers between Android and Linux went**.

The experience was pretty similar to what I found on the Linux app, with tight integration with Android's “*Share*” functionality, that allowed me to directly share files from the gallery app of my phone.

{% image https://news.itsfoss.com/content/images/size/w1000/2024/07/localsend-android-2.jpg Sending files from Android to Ubuntu using LocalSend %}

Before I accepted the transfer on my Ubuntu laptop, I could rename the files, and remove the ones I didn't want.

![a screenshot of localsend after a successful file transfer session with the size and speed being shown below](https://news.itsfoss.com/content/images/2024/07/LocalSend_m.png)

After the transfer was complete, I clicked on the “*Advanced*” option to see the speeds it went to, and it was good, seeing those were just .jpg files.

Finally, I checked how **file transfers between Linux and Windows worked**.

I booted up a Windows 10-equipped [virtual machine](https://itsfoss.com/virtual-machine/), and installed the official .exe for it. When I started the app, it was showing me three different “*Big Banana*” devices, I went with the first one, and started transferring two .exe files that were already present.

{% grid c:2 %}
<!-- cell -->
{% image https://news.itsfoss.com/content/images/2024/07/LocalSend_n.png %}
<!-- cell -->
{% image https://news.itsfoss.com/content/images/2024/07/LocalSend_p.png %}
<!-- cell -->
{% image https://news.itsfoss.com/content/images/size/w1000/2024/07/LocalSend.png %}
<!-- cell -->
{% image https://news.itsfoss.com/content/images/size/w1000/2024/07/LocalSend_q.png %}
<!-- cell -->
Sending files from Windows to Ubuntu using LocalSend
{% endgrid %}

The transfer was a success, and I didn't face any problems, with transfer speeds going up to 40 MB/s.

As for the weird three-device issue, my best bet is that it was a bug caused by me running a VM on the same device, and it probably also had to do something with how VirtualBox handles networking.

{% note color:cyan 📋 I also tried the messaging feature with LocalSend, it worked well. I could also send installed apps (**as .APKs**) from my smartphone to other devices.  %}

## Closing Thoughts

Overall, **my experience with LocalSend was great!** I have now installed it on all my devices to facilitate wireless file transfers. 😃

Though, **smaller transfers are the way to go with this app**. As I tried a ~90 GB transfer from my Ubuntu laptop to my Android tablet, and the speeds were fluctuating a lot, in the end, the transfer just stopped due to a connection error.

But, in comparison to [KDE Connect](https://kdeconnect.kde.org/), I would say that LocalSend is a better option for file transfers. I say that due to its more intuitive user experience and comparable transfer speeds, that ought to catch on with most users.

## 📥 Get LocalSend

You can get LocalSend for a wide range of devices, such as **Linux**, **Android**, **Windows**, **iOS**, and **macOS**.

For Linux users, they can get it from the [Flathub store](https://flathub.org/apps/org.localsend.localsend_app), for Android, the [Play Store](https://play.google.com/store/apps/details?id=org.localsend.localsend_app&), and for iOS/iPadOS/macOS, the [App Store](https://apps.apple.com/us/app/localsend/id1661733229).

Those who are looking for alternative packages can head to the [official website](https://localsend.org/download) or its [GitHub](https://github.com/localsend/localsend/) repo.

<center>{% button "LocalSend" https://localsend.org/download %}</center>

*💬 Do let me know if you know of other similar tools in the comments below!*
