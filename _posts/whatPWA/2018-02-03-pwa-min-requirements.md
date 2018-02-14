---
layout: post
title:  "PWA Minimum Requirements"
date:   2018-02-03 18:07:15 -0800
categories: What is a PWA
---
# PWA Minimum Requirements

In order to build a Progressive Web App, the following minimum requirements should be met:

 - **Secure**. A secure connection (HTTPS) over your site makes sure all traffic is as safe as a native app. A secure endpoint also allows the service worker to securely take action on the behalf of your app.

 - **Standard Manifest**. The site should be controlled by a W3C manifest that determines the experience and behavior of your PWA. This includes everything from images, to language, to the start page of your web app.

 - **Network Independent**. The Progressive Web App should have a mechanism (e.g. through a service worker) to help control traffic when the network isn't there or isn't reliable. The app should be able to work independent of network.

 - **Responsiveness**. The site should be responsive on tablets & mobile devices.

 - **Cross-Browser**. The site should work in multiple browsers (e.g. Chrome, Edge, Firefox and Safari).

 - **Deep Linking**. Each page of the site should have an unique URL (individual pages are deep linkable via URLs e.g. to share on social media).

The quick start will provide the tools to address some of the above requirements, like building the W3C manifest and enabling network independence. However, it is responsibility of the site developer to fulfill the other requirements.