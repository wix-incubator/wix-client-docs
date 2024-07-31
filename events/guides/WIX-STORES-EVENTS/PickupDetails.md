# Pickup Details

Triggered when the user enters pickup information and clicks to advance to the next step in the checkout flow.


**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Wix category|
|eventAction|text|More detailed event name|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product name|
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent(‘CustomEvent’, 
  {
    "eventCategory": "Enhanced Ecommerce  - Stores",
    "eventAction": "Pickup Details",
    "eventLabel": "Stores",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
  }
```
