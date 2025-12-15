# Start Payment

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when the user gets to the payment part of the checkout funnel.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e Stores, Bookings |
|contents|array|All products in cart|  
|contents.id|text|Product ID|
|contents.name|text|Product name|
|contents.category|text|Collection name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product price|
|contents.currency|currency|Currency in ISO-4217 format|


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
