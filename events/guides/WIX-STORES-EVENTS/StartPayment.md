# Start Payment

Triggered when the user gets to the payment part of the checkout funnel.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e Stores, Bookings |
|contents|Array|All products in cart|  
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|contents.category|text|Collection Name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product Price|
|contents.currency|currency|default site currency in ISO-4217 format|


**Example**:
```JSON
trackEvent("StartPayment", 
  {
    "origin": "Stores",
    "option": "Express",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
  }
```
