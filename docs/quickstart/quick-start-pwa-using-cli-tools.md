# Quick Start PWA using CLI tools

This quick start walks you through the steps to create a Progressive Web App (PWA) from scratch using the **pwabuilder CLI Tools**. Make sure you meet the [minimum requirements](../whatPWA/pwa-min-requirements.md).

The first step is to build the Manifest for your application using the **pwabuilder CLI Tools**. The builder will search in the home page of your site looking for information about the app in specific meta tags. For more information, read [What is a Manifest](../whatPWA/what-is-a-manifest.md).

## Manifest
The Manifest for Web Apps is a JSON-based manifest file that provides a centralized place to put metadata associated with a web application (like app name, icons, presentation, etc.), thus solving the problem of having to maintain an heterogeneous set of meta tags and link tags to support each platform. PWAs use this manifest to control the appearance and behavior of the app when it is installed and launched from the user device. For more details see the Web App Manifest Specification.

### Install the Tools
Before installing **pwabuilder CLI Tools**, you must first install [Node.js](https://nodejs.org/) (version 0.12.0 or later).

1. Open a command prompt or terminal window and type the following command:  

    `npm install pwabuilder -g`

### Generate Manifest
The **pwabuilder CLI Tools** will search in the home page of your site looking for an existing manifest. If not, it will gather information about the app in specific meta tags or propose default values for the manifest properties. It will also show any warnings or suggestions to address potential issues in the collected metadata. Make sure you address any warnings before you move on.

**Usage:**
`pwabuilder <website-url> [options]`

**Example:**
`pwabuilder https://btdj.azurewebsites.net/ -d C:\Projects -l debug -p windows10,android`

![Generate Manifest](images/quickstart-pwa-cli-generate-manifest.png)

## Service Workers
During this step you will choose functionalities you want to add to your app. You will include code to use sample service workers implementing those features from a repository. Learn more about service workers [here](../whatPWA/what-is-a-service-worker).

### Build Service Worker
1. Open a browser and navigate to the [serviceworkers](https://github.com/pwabuilder/serviceworkers) repository
2. In this repository you will find sample code of service workers implementing the following features:
	- Offline page (location: [/ServiceWorker1](https://github.com/pwabuilder/serviceworkers/tree/master/serviceWorker1) folder)
	- Offline copy of pages (location: [/ServiceWorker2](https://github.com/pwabuilder/serviceworkers/tree/master/serviceWorker2) folder)
	- Combination of offline page + offline copy of pages (location: [/ServiceWorker3](https://github.com/pwabuilder/serviceworkers/tree/master/serviceWorker3) folder)
3. Download the service worker files including the code for your website and the service worker code
	1. pwabuilder-sw-register.js registers the service worker for the website
	2. pwabuilder-sw.js is the service worker's code
4. The code for your website should be included in your HTML to register the service worker

![Code for Website](images/quickstart-pwa-cli-code-for-website.png)

5. Upload the service worker code JS file to the web site

![Service Worker Code](images/quickstart-pwa-cli-service-worker-code.png)

## Publishing
Publishing your Progressive Web App is mainly a matter of adding the W3C manifest file and service worker scripts to your website. These assets are then referenced from your website, both with a link tag reference to the manifest file and the service worker registration scripts.

### Web
1. This is still a web app, so step one is to include these new files into your web site. You can grab file created in the _Generate Manifest_ step and the script files in the _Build Service Worker_ step
2. Add and upload them to your website. Different browsers will detect your Progressive Web App in different ways, but the **manifest** and **service workers** are required for each of them. 
	- The Web App Manifest is deployed in your HTML pages using a **link** tag in the head of your document: `<link rel="manifest" href="/manifest.json">`.
	- Also, add and upload references **images** and **service worker** files to the root path of the site.

### Windows
Windows 10 PWA support is still in Beta, so some features like service workers will not work on all user machines. Your PWA can be created and app listing generated for supported platforms (using the -p option, in this case windows10).

**Example:**
`pwabuilder package C:\Projects\HotBeats -p windows10 -a -l debug`

![Service Worker Code](images/quickstart-pwa-cli-publish-windows10.png)

### Android
Publishing directly to the Android Play Store will be coming soon.

### Other
You can now generate the polyfill packages to publish both Android and iOS. You'll need Xcode to build and submit your package to the Store.


## Polyfills
Given that not every platform or browser runs PWAs yet, the builder provides polyfills for platforms that lack support like [iOS](../tools/how-to-package-ios.md), [Mac](../tools/how-to-package-mac.md) and [Windows 7](../tools/how-to-package-windows7.md).
In case of Android, PWAs are available through the browser; however, you can generate an [Android](../tools/how-to-package-android.md) polyfill app that can be also submitted to the Play store.

### Android
1. In case you haven't done in the previous step, you can generate the polyfills for Android executing: `pwabuilder https://btdj.azurewebsites.net/ -p android`
2. Then, follow the [instructions](../tools/how-to-package-android.md) to publish your Android app.

### iOS
1. In case you haven't done in the previous step, you can generate the polyfills for iOS executing: `pwabuilder https://btdj.azurewebsites.net/ -p ios`
2. Then, follow the [instructions](../tools/how-to-package-ios.md) to publish your Android app.

### MacOS

1. Follow the [instructions](../tools/how-to-package-mac.md) to publish your MacOS app.

### Windows 7

1. Follow the [instructions](../tools/how-to-package-windows7.md) to publish your Windows 7 app.