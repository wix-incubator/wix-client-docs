# Add to Cart

Triggered when user clicks on the ‘Add to cart’ button.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|category|text|Collection name|
|origin|text|Wix App name, i.e stores, bookings |
|id|text|Product ID|
|name|text|Product name|
|variant|text|Selected choice from 1st product option|
|price|currency|Product price|
|currency|currency|Currency in ISO-4217 format|
|quantity|number|Quantity of product added to cart|
|sku|text|Product SKU|
|type|text|Product type: physical or digital|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metasiteId|text|Wix site ID|

**Example**:
```JSON
{
  "category": "All Products",
  "origin": "Stores",
  "id": "cd59cd36-b6d2-2cf3-9d48-81793a7bdbbd",
  "name": "Reading glasses",
  "price": 20,
  "currency": "USD",
  "quantity": 1,
  "sku": "364215375135191",
  "type": "physical",
  "isPremium": true,
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661",
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```
