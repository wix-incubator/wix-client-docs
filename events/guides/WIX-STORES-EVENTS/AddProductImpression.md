# Add Product Impression

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered whenever a page is loaded that contains either a product gallery or widget.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|contents|array|All purchased products |  
|contents.id|text|Product ID|
|contents.name|text|Product name|
|contents.list|text|Name of relevant product gallery|
|contents.category|text|Collection name|
|contents.position|number|Product position in the gallery|
|contents.price|currency|Product price|
|contents.currency|currency|Currency in ISO-4217 format|
|origin|text|Wix App name, i.e Stores, Bookings |  
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:  
```json
{
  "contents": [{
    "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e", 
    "name": "Shoes", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 0, 
    "price": 85,
    "currency": "USD"
  },
  {
    "id": "cd59cd36-b6d2-2cf3-9d48-81793a7bdbbd", 
    "name": "Reading glasses", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 1,
    "price": 20,
    "currency": "USD"
  },
  {
    "id": "c8539b66-7a44-fe18-affc-afec4be8562a", 
    "name": "Watch", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 2,
    "price": 10,
    "currency": "USD"
  }],
  "origin": "Stores", 
  "isPremium": true, 
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661", 
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```
