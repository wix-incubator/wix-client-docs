# Remove from Cart

Triggered when the user clicks to remove an item from the cart.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e stores, bookings |
|id|text|Product ID|
|name|text|Product Name|
|category|text|Collection Name|
|variant|text|Selected choice from 1st product option|
|price|currency|Product price|
|currency|currency|default site currency in ISO-4217 format|
|quantity|integer|Quantity of product added to cart|
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
