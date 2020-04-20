# Delivery Method

Triggered when the user adds personal information and clicks to advance to the next step in the checkout flow.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Wix category|
|eventAction|text|More detailed event name|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", 
  {
    "eventCategory": "Enhanced Ecommerce - Stores",
    "eventAction": "Add Delivery Method",
    "eventLabel": "stores",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
  }
```
