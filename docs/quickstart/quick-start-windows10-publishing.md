# Quick Start Windows 10 Publishing
Publishing your Progressive Web App is mainly a matter of adding the W3C manifest file and service worker scripts to your website. These assets are then referenced from your website, both with a link tag reference to the manifest file and the service worker registration scripts.

Windows 10 PWA support is still in Beta, so some features like service workers will not work on all user machines. 

## Publish through website
Your PWA can be created and app listing generated from the below one step publishing button.

1. Click **Publish 1-step** button under the Windows panel
2. Enter the user name or company name and a valid email address

    ![Publish Package](images/quickstart-pwa-website-publish-package.png)

3. Click **Submit**.

## Publish via CLI
Your PWA can be created and app listing generated for supported platforms (using the -p option, in this case windows10).

**Example:**
`pwabuilder package C:\Projects\HotBeats -p windows10 -a -l debug`

![Service Worker Code](images/quickstart-pwa-cli-publish-windows10.png)



