---
layout: post
title:  "Quick Start Windows 10 Publishing"
date:   2018-02-03 18:07:25 -0800
categories: Quickstart
---

# Quick Start Windows 10 Publishing
Publishing your Progressive Web App is mainly a matter of adding the W3C manifest file and service worker scripts to your website. These assets are then referenced from your website, both with a link tag reference to the manifest file and the service worker registration scripts.

Windows 10 PWA support is still in Beta, so some features like service workers will not work on all user machines. 

## Self Publish through Windows Dev Center
You can easily create a listing for your PWA within the Microsoft Store on Windows 10.  Your PWA package can then be uploaded for users to discover

1. Obtain a [Windows Dev Account](https://dev.windows.com).  The PWA builder team has a limited number of account tokens that can be used by web developer to cover the cost of a dev account with Microsoft for the beta.  Reach out to jeffburt@microsoft.com or @boyofgreen on twitter for a code.

2. Login to dev.windows.com and start a "new app" to reserve the name of your app.  ** You must use the same name as the "name" or "short_name" on your W3C manifest.** The dev center will tell you if the name is not available.

3. In the Windows 10 Dev center, find the "publisher dispaly name", "Publisher Identity" and "Package Indentity Name" of your app. You'll find it under App Management > App Identity

4. Go to preview.pwabuilder.com and enter your url. 

5. On step 3, choose "generate Appx" and enter the info the requested info from the dev center.

6. Find appx named "windows.appx" in a new directory named "packages" in \PWA\Store packages\windows10

7. Go back to the dev center and upload the Appx from pwabuilder .

## Publish via CLI
Your PWA can be created and app listing generated for supported platforms (using the -p option, in this case windows10).

**Example:**
`pwabuilder package C:\Projects\HotBeats -p windows10 -a -l debug`

![Service Worker Code](/assets/quickstart-pwa-cli-publish-windows10.png)



