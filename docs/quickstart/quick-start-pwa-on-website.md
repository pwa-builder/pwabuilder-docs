# Quick Start PWA on Website

This quick start walks you through the steps to create a Progressive Web App (PWA) from scratch using the **pwabuilder.com** builder site. Make sure your website meets the [minimum requirements](../whatPWA/pwa-min-requirements.md).

The first step is to build the Manifest for your application using the **pwabuilder.com** web site. The builder will search in the home page of your site looking for information about the app in specific meta tags. For more information, read [What is a Manifest](../whatPWA/what-is-a-manifest.md).

### Provide a URL

1. Open a browser and navigate to [https://preview.pwabuilder.com](https://preview.pwabuilder.com)
2. Click on the **Get Started** button
3. In the URL textbox, enter the URL of your site and click on **Get Started** again
	
	![Provide a URL](images/quickstart-pwa-website-provide-a-url.png)
	
### Generate Manifest
The builder will search in the home page of your site looking for an existing manifest. If not, it will gather information about the app in specific meta tags or propose default values for the manifest properties. It will also show any warnings or suggestions to address potential issues in the collected metadata. Make sure you address any warnings before you move on.

**Note:** If your site already has a manifest in place and you are comfortable with the current manifest data, you can skip this step and click on **Next step** at the right top of the wizard to jump directly to the **Build Service Worker** step.

![Generate Manifest](images/quickstart-pwa-website-generate-manifest.png)


#### Add Images
The builder site also checks whether the manifest has defined the expected icon sizes for the different platforms (Windows, Android, iOS) and helps to generate the missing sizes. You can also generate missing image sizes for other platforms using the [PWA Image Generator](http://appimagegenerator-pre.azurewebsites.net/).

1. In our example, we don't have any image defined in the manifest so we'll proceed uploading an image with our app logo. To do this, click on the **Upload an image…** link at the left pane. Browse to the location of the image to upload and, if you want to generate the missing sizes, make sure the **Generate missing images from this image** checkbox is marked.

    **Note:** Currently, the **Upload image** option will only generate the required image sizes for Windows 10.
	
    ![Upload an Image](images/quickstart-pwa-website-upload-an-image.png)
	
2. Click **Submit**. In our example, the missing image sizes are automatically generated and added to the manifest.
	
	![Images Preview](images/quickstart-pwa-website-images-preview.png)
	
#### Download Manifest
Once you are done with the updates to the manifest you can download the web app manifest here. Also, you can move on to build a Service Worker and/or Publish your PWA in the next steps.

## Service Workers
During this step you will choose functionalities you want to add to your app. The builder will include code to use sample service workers implementing those features from a repository. Learn more about service workers [here](../whatPWA/what-is-a-service-worker.md).

By default, the builder includes the Offline page service worker to pull a file from your web server called "offline.html" and serve the file whenever a network connection cannot be made.
Additionally, you can select the Offline copy of pages service worker to keep a cache of all visited pages and serve the stored version in case any fetch fails. Also, the builder can include both features into a combined service worker for a full offline experience.

1. Select the functionalities you want to include in your application
	
	![Select Service Workers](images/quickstart-pwa-website-select-service-workers.png)
	
	
2. Download the service worker package including the code for your website and the service worker code
3. The code for your website should be included in your HTML to register the service worker
	
	![Code for Website](images/quickstart-pwa-website-code-for-website.png)
	
	
4. Upload the service worker code JS file to the web site
	
	![Service Worker Code](images/quickstart-pwa-website-service-worker-code.png)
	

## Publishing
Publishing your Progressive Web App is mainly a matter of adding the W3C manifest file and service worker scripts to your website. These assets are then referenced from your website, both with a link tag reference to the manifest file and the service worker registration scripts.

### Web
1. This is still a web app, so step one is to include these new files into your web site. You can click the **Download** button of the Web section to get the files that you need to add to your site.
2. Add and upload them to your website. Different browsers will detect your Progressive Web App in different ways, but the **manifest** and **service workers** are required for each of them. 
		○ The Web App Manifest is deployed in your HTML pages using a **link** tag in the head of your document: `<link rel="manifest" href="/manifest.json">`.
		○ Also, add and upload references **images** and **service worker** files to the root path of the site.

### Windows
Windows 10 PWA support is still in Beta, so some features like service workers will not work on all user machines. Your PWA can be created and app listing generated from the below one step publishing button.

1. Click **Publish 1-step** button under the Windows panel
2. Enter the user name or company name and a valid email address
	
	![Publish Package](images/quickstart-pwa-website-publish-package.png)
	
3. Click **Submit**.

### Android
Publishing directly to the Android Play Store will be coming soon.

### Other
You can now download polyfill packages to publish both Android and iOS. You'll need Xcode to build and submit your package to the Store.

![Platforms](images/quickstart-pwa-website-platforms.png)


## Polyfills
Given that not every platform or browser runs PWAs yet, the builder provides polyfills for platforms that lack support like [iOS](../tools/how-to-package-ios.md), [Mac](../tools/how-to-package-mac.md) and [Windows 7](../tools/how-to-package-windows7.md).
In case of Android, PWAs are available through the browser; however, you can generate an [Android](../tools/how-to-package-android.md) polyfill app that can be also submitted to the Play store.

### Android
1. In the **Publish PWA** step of the builder wizard, locate the **Android** section and click the **Download** button. The app package will be generated and downloaded to your local drive.

![Android Polyfill](images/quickstart-pwa-website-android-polyfill.png)

2. Then, follow the [instructions](../tools/how-to-package-android.md) to publish your Android app.

### iOS
1. In the **Publish PWA** step of the builder wizard, locate the **iOS Polyfill** section and click the **Download** button. The app package will be generated and downloaded to your local drive.

![iOS Polyfill](images/quickstart-pwa-website-ios-polyfill.png)

2. Then, follow the [instructions](../tools/how-to-package-ios.md) to publish your iOS app.

### Mac
Not supported on the website. See "QuickStart PWA via CLI"

### Win7
Not supported on the website. See "QuickStart PWA via CLI"