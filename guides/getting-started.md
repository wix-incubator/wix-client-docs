# Introduction

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Our client-side APIs are a collection of events and APIs that can be used by any integration that injects JavaScript into a Wix site using the [Embedded Script extension](https://dev.wix.com/docs/build-apps/develop-your-app/extensions/site-extensions/embedded-scripts/about-embedded-scripts).

The events can give your app real-time information about the site, the content viewed, and user actions.
This reference documents every object and method available. You can use these APIs to make your app react to user actions or learn about user behavior. In addition, you can use the API to report and listen to custom events sent by other apps.


## On-Ready Event
To make sure you aren't calling the event before it is fully initiated, here is an on-ready event you can listen to:
```JavaScript
function registerListener() {
    window.wixDevelopersAnalytics.register('head', 
      (eventName, eventParams) => console.log('wix dev head', eventName, eventParams));
}

window.wixDevelopersAnalytics ?
  registerListener() :
 window.addEventListener('wixDevelopersAnalyticsReady', registerListener);  
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
