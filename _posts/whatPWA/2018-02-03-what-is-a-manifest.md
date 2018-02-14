---
layout: post
title:  "What is a Manifest"
date:   2018-02-03 18:07:15 -0800
categories: What is a PWA
---

# What is a Manifest

The Manifest for Web Apps is a JSON-based manifest file that provides a centralized place to put metadata associated with a web application (like app name, icons, presentation, etc.), thus solving the problem of having to maintain an heterogeneous set of meta tags and link tags to support each platform. PWAs use this manifest to control the appearance and behavior of the app when it is installed and launched from the user device. For more details see the [Web App Manifest Specification](http://www.w3.org/TR/appmanifest/).

The Manifest can use as many or as few of the declarations as is needed.  A sample manifest looks like the below:

```javascript

{
  "dir": "ltr",
  "lang": "en",
  "name": "Bing",
  "scope": "/",
  "display": "browser",
  "start_url": "https://www.bing.com/",
  "short_name": "Bing",
  "theme_color": "#4F4F4F",
  "description": "Bing helps you turn information into action, making it faster and easier to go from searching to doing.",
  "orientation": "any",
  "background_color": "transparent",
  "related_applications": [],
  "prefer_related_applications": false,
  "icons": [
    {
      "src": "/fd/s/a/hp/bing.svg",
      "sizes": "any",
      "type": "image/svg+xml"
    }
  ]
}



```