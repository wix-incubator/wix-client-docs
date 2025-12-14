# Site Members Sign up / Log in Tracking

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>x

Triggered when a user signs up or logs in to Wix Members.

**Properties**:  

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Wix category |  
|eventAction|text|Sign up Success / Sign up Submit / Sign up Failure / Log in Success / Log in Submit / Log in Failure|  
|eventLabel|text|Origin (Facebook/Google/Wix)|  
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|  

**Example**:
```JSON
trackEvent("CustomEvent", {
    "eventCategory" : "Site members",
    "eventAction" : "Sign up Success",
    "eventLabel": "Facebook" 
} );
```
