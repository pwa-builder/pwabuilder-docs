# What is a Service Worker

Service workers are scripts that your browser runs in the background and act as a network proxy in the web browser to manage the web/HTTP requests programmatically. It's fairly easy to add a service worker to your website.  "Register" your service worker and set the scope:

```javascript

navigator.serviceWorker.register('pwabuider-sw.js', {
    scope: './'
  })


```

Service Workers lie between the network and device to supplement the content enabling the creation of effective offline experiences using the cache mechanisms. They will also allow access to push notifications and background sync APIs. A service worker looks something like this:

```javascript

//This is the "Offline page" service worker

//Install stage sets up the offline page in the cache and opens a new cache
self.addEventListener('install', function(event) {
  var offlinePage = new Request('offline.html');
  event.waitUntil(
  fetch(offlinePage).then(function(response) {
    return caches.open('pwabuilder-offline').then(function(cache) {
      console.log('[PWA Builder] Cached offline page during Install'+ response.url);
      return cache.put(offlinePage, response);
    });
  }));
});


```