# Quick Start Windows 10 Publishing
Publishing your Progressive Web App is mainly a matter of adding the W3C manifest file and service worker scripts to your website. These assets are then referenced from your website, both with a link tag reference to the manifest file and the service worker registration scripts.

Windows 10 PWA support is still in Beta, so some features like service workers will not work on all user machines. 

## Self Publish through Windows Dev Center
You can easily create a listing for your PWA within the Microsoft Store on Windows 10.  Your PWA package can then be uploaded for users to discover

1. Obtain a [Windows Dev Account](https://dev.windows.com).  The PWA builder team has a limited number of account tokens that can be used by web develper to cover the cost of a dev account with Microsoft for the beta.  Reach out to jeffburt@microsoft.com or @boyofgreen on twitter for a code.

2. Login to dev.windows.com and start a "new app" to reserve the name of your app.  ** You must use the same name as the "name" or "short_name" on your W3C manifest.** The dev center will tell you if the name is not available.

3. In the Windows 10 Dev center, find the "publisher name", "Publisher Identity" and "Package Family Name" of your app. You'll find it under *******************

4. Go to preview.pwabuilder.com and enter your url. 

5. On step 3, choose "generate Appx" and enter the info the requested info from the dev center.

6. Go back to the dev center and upload the Appx from pwabuilder .

## Publish via CLI
Your PWA can be created and app listing generated for supported platforms (using the -p option, in this case windows10).

**Example:**
`pwabuilder package C:\Projects\HotBeats -p windows10 -a -l debug`

![Service Worker Code](images/quickstart-pwa-cli-publish-windows10.png)



