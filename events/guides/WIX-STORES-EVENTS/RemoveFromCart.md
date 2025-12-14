# Remove from Cart

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when the user clicks to remove an item from the cart.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e Stores, Bookings |
|id|text|Product ID|
|name|text|Product name|
|category|text|Collection name|
|variant|text|Selected choice from 1st product option|
|price|currency|Product price|
|currency|currency|Currency in ISO-4217 format|
|quantity|number|Quantity of product removed from cart|
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
   "name": "Soundbeam ERD - 3083",
   "category": "All Products",
   "currency": "ILS",
   "price": 220,
   "quantity": 2,
   "sku": "00001",
   "type": "physical",
   "isPremium": true,
   "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
   "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"    
}
```
