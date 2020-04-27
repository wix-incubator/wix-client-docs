Our client-side APIs are a collection of events and APIs that can be used by any integration that injects JavaScript into a Wix site using the Embedded Script component (learn more about Embedded Script component).

The events can give your app real-time information about the site, the content viewed, and user actions.
This reference documents every object and method available. You can use these APIs to make your app react to user actions or learn about user behavior. In addition, you can use the API to report and listen to custom events sent by other apps.


## On-Ready Event
To make sure you aren't calling the event before it is fully initiated, here is an on-ready event you can listen to.
Once it is initiated, register your app to the events using the register function. The register function requires two parameters:
* app_id (String) - register using your app id to make sure each app is registered once, and for our records
* callback (Function) - a callback function to invoke on an event accrues. The callback function will receive an event name as a string and an object with the event data.
```JavaScript
function registerListener() {
    window.wixDevelopersAnalytics.register('head', 
      (eventName, eventParams) => console.log('wix dev head', eventName, eventParams));
}

window.wixDevelopersAnalytics ?
  registerListener() :
  window.onWixDevelopersAnalyticsReady = function() {
    registerListener();
  }
```

## Listening to a Predefined Wix Event

Add this code to your embedded script component, and make sure to point to the events you are interested in:

```JavaScript
window.wixDevelopersAnalytics.register('app-ID', function report(eventName, data) { 
  switch(eventName) { 
    case 'pageview':
      callMyPageViewFunction(data); 
      break; 
    case 'addToCart':
      callMyAddToCartFunction(data); 
      break;
  }
}
```
