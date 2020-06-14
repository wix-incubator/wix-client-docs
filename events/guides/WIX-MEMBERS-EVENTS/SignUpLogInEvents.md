# Site Members Sign up / Log in Tracking

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
