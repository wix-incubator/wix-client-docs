# Click Product

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when the user clicks on a product from any of the galleries.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|id|text|Product ID|
|origin|text|Wix App name, i.e Stores, Bookings |
|name|text|Product name|
|list|text|Name of relevant product gallery|
|category|text|Collection name|
|position|number|Product position in the gallery|
|price|currency|Product price|
|currency|currency|Default site currency in ISO-4217 format|
|sku|text|Product SKU|
|type|text|Product type: physical or digital|
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
  "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e",
  "origin": "Stores",
  "name": "Shoes",
  "list": "Grid Gallery",
  "category": "All Products",
  "position": 1,
  "price": 85,
  "currency": "USD",
  "type": "physical",
  "sku": "364215376135191",
  "isPremium": true,
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661",
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```

