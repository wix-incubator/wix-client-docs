# Shipping Details

Triggered when the user adds shipping details and clicks to advance to the next step in the checkout flow.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Wix category|
|eventAction|text|More detailed event name|
|eventLabel|text|Wix App name, i.e Stores, Bookings (equivalent to `origin`)|
|contents|array|All purchased products|
|contents.id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent(‘CustomEvent’, 
  {
    "eventCategory": "Enhanced Ecommerce",
    "eventAction": "Add Shipping Details",
    "eventLabel": "Stores",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }],
    "isPremium": true,
    "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
    "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"
  }
```
