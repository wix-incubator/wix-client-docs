# Agree to Terms

Triggered when the user check the Agree to terms & conditions’ checkbox.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Wix category|
|eventAction|text|More detailed event name|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.id|text|Product ID|
|contents.name|text|Product name|
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent(‘CustomEvent’, 
  {
    "eventCategory": "Enhanced Ecommerce",
    "eventAction": "Agree To Terms",
    "eventLabel": "Stores",
    "contents":[{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
 }
```
