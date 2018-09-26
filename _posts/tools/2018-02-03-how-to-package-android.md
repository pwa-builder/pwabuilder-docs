---
layout: post
title:  "How to Package Android"
date:   2018-02-03 18:07:25 -0800
categories: jekyll update
---

# How to Package Android

1. In the **Publish PWA** step of the builder wizard, locate the **Android** section and click the **Download** button. The app package will be generated and downloaded to your local drive.
	
    ![Android Polyfill](/assets/android-polyfill.png)

2. Extract the package into a local folder

3. Open the project in Android Studio
    1. Download and install the [Java SDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)

    2. [Download](http://developer.android.com/sdk/installing/index.html?pkg=studio) and install Android Studio and the Android SDK

    3. Open Android Studio and select the **Import project** option. Select the folder **projects/Polyfills/android/source** and click **OK**.

        **Note:** The version of Gradle installed by Android studio might not be compatible with the project's Gradle configuration. If that is the case, Android Studio will show an error and provide an option to fix/upgrade the project.

4. Test the project

    1. In Android Studio, select **Run > Run** in the menu bar to build and run the app

    2. If it is the first time running the app, Android Studio asks to select a deployment target. Select a device or emulator to install and run the app

5. Build the project

    1. Select the build variant (debug|release) from the **Build Variants** window
   
    2. In Android Studio, select **Build > Build APK** in the menu bar. The APKs are saved in **projects/Polyfills/android/build/outputs/apk/**


		**Note:** Before you can generate a release version of your app for public distribution, you must [sign your APK](https://developer.android.com/tools/publishing/app-signing.html)

6. Submit the app to the Store

    1. Go to the [Google Play Developer Console](https://play.google.com/apps/publish/signup/)

    2. Follow the steps to:

        1. Setup an Android Developer account

        2. Reserve a name for your app

        3. Upload your app package
