﻿Title: How to distribute your enterprise mobile app?
Summary: If you have developed an enterprise mobile app, for example, an app that connects with the company database and show some reports, how can you safely distribute it?
Tags: Android, iOS
Date: OCT 04, 2015
URL: how-to-distribute-your-enterprise-mobile-app

Publishing Android and iOS apps are quite easy if your app is designated to the general public. You just need to register in the store, Google Play or App Store, follow some steps and publish it. These stores also handle the distribution of new versions in the comfortable automatic update solution.

However, if you are deploying a private enterprise app, for example, something the connects with the company database to input some info or show some reports, you don't want to make it public, neither Google or Apple. So, what are your options?

## Android

### Distributing your app in-house

When you build an Android app, you get a file with the .apk extension. If you distribute this file to your employees, they can download it using their Android device and easily install the app using a file manager, like [ES File Explorer](https://play.google.com/store/apps/details?id=com.estrongs.android.pop) or [Astro](https://play.google.com/store/apps/details?id=com.metago.astro).

This distribution can be done in the company's intranet, Sharepoint, FTP or something similar. The tricky part is to handle app updates automatically. You'll need to implement, for each app, a listener or pooling mechanism to watch for updates. Otherwise, you'll need to send periodic e-mails requesting employees to grab and update their apps.

As you can see, this approach looks like *free*, but actually is not. You'll waste many admin hours to develop/handle this kind of solution. So, usually, a paid solution may be better.

### Google Play

Google offers their store to be used privately by companies. Starting by [$5 per user per month](https://www.google.com/intx/en/work/apps/business/pricing.html), you can create a [private channel](https://support.google.com/a/answer/2494992?hl=en) and add your employees accounts. To access the channel, they need to go to Play Store > Apps > Categories > [your organization's name] on their Android device. Automatic updates are obviously supported.

## iOS

### Distributing your app in-house

As Apple doesn't follow Google's openness nature, you can't simple build and distribute your app. You need to pay to Apple a [$299 per year](https://developer.apple.com/programs/enterprise/) fee to enroll for [Apple Developer Enterprise Program](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/DistributingEnterpriseProgramApps/DistributingEnterpriseProgramApps.html). Furthermore, you need use a MDM (Mobile Device Management) System to distribute your iOS apps (.ipa extension).

## App Store

Unfortunately, you can't have a private channel at App Store. If you deploy your apps there, it'll be public and need to follow Apple's guideline. As it'll probably be of restricted access, it'll not be accepted.

## Other Options

### Mobile Device Management

A MDM solution requires a server to be responsible for storing the apps deploys and a client to be installed in each device. A MDM is the best approach when security is a deep concern since the company can take control of the device and allow only selected programs to be installed. Usually, the device will have full disk encryption and the administrators will have the ability to remote wipe all data in case of loss or theft of the device. Jailbroken (iOS) and rooted (Android) devices can also be detected and their access to the companies' services can be revoked since those poses a significant risk.

For examples of MDM solutions, you can read more about [AirWatch](http://www.air-watch.com/), [Symantec](http://www.symantec.com/mobility/implement.jsp), [Appearian](https://www.apperian.com/mam-blog/comparing-ios-android-mdm-protocol-design-philosophies/) and [MasS360](http://www.maas360.com/).

### Virtualization

Virtualization is a new kind of distribution that is growing in attention. It offers the worst user experience, since network latencies and connections problems affects the usage, but is used when the security concerns of data leak are too frightening.

### Web-Based Apps

Another option is to use web-based apps instead of native. This is a very hard decision and a never-ending debate with pros and cons, but in this case, since it doesn't need a online store for updates, "distributing" is much easier.
