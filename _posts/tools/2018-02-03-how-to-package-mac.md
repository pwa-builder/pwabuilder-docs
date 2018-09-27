---
layout: post
title:  "How to Package MacOS"
date:   2018-02-03 18:07:25 -0800
categories: jekyll update
---

At this time you cannot build the MacOS app via the PWA Builder website, so you'll need to build this app via the CLI tool. MacOS is supported in the [macOS platform module](https://www.npmjs.com/package/pwabuilder-macos) for pwabuilder.

# How to Package MacOS using CLI Tools

1. Make sure **pwabuilder** installed. If not, install using: 

`npm install -g pwabuilder`

2. Then, use pwabuilder to generate the polyfills: 

'pwabuilder https://btdj.azurewebsites.net/ -d C:\Projects -l debug -p MacOS'

  Parameter |  Description
 --- | --- 
 *-d* | the directory you would like to generate the app
 *-l* | the log level of the CLI
 *-p* | the platforms to build


 

**Note** if you would like to submit the app to the mac store, continue on with step 4 and 5


4. You'll need to download and install [Xcode](https://developer.apple.com/xcode/downloads/)

5. Then, you can follow the[ Submitting Your App to the Store](https://developer.apple.com/library/content/documentation/IDEs/Conceptual/AppDistributionGuide/SubmittingYourApp/SubmittingYourApp.html) steps in the Apple's App Distribution Guide.
