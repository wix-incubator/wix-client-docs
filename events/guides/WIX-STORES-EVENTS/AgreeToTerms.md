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
|contents.name|text|Product Name|
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

### Pickup Details

Triggered whenthe user enters pickup information and clicks to advance to the next step in the checkout flow.


**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Fixed ‘Enhanced Ecommerce’ string(???)|
|eventAction|text|Fixed ‘Add Shipping Details’ string|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
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
