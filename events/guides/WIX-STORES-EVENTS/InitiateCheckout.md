# Initiate Checkout

Triggered when the **Checkout** button is clicked. ???

## Initiate Checkout: Event Properties

<!-- |Name|Type|Description|  
|---|---|---|  
|contents|array|All products in cart|  
|contents.id|text|Product ID|
|contents.name|text|Product name|
|contents.category|text|Collection name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product price|
|contents.currency|currency|Currency in ISO-4217 format|
|contents.quantity|number|Quantity of product added to cart|
|origin|text|Wix App name, i.e Stores, Bookings |  
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID| -->

| Name | Type  | Description |  
| --- | --- | --- |
| origin  | string  | Wix App that emitted this event, such as "Stores", "Bookings" |
| id | GUID  | Product ID  |
| name  | string  | Product name  |
| price  | number | Total price of all items currently in cart  |
| currency  | currency  | Currency in ISO-4217 format  |
| quantity  | number  | Number of items in cart  |
| sku  | string  | Product Stock Keeping Unit (SKU)  |
| type  |  string | Product type (for example, "physical") |
| brand  |  string | Product brand  |
| checkoutId  | GUID  | Checkout ID  |
| contents  | array of objects  | All products in cart  |
| contents.id  | GUID  | Product ID  |
| contents.name  | string  | Product name |
| contents.price  | number  | Product price |
| contents.currency  | currency  | Currency in ISO-4217 format  |
| contents.quantity  | number  | Product quantity  |
| visitorId  |  GUID | Site visitor ID |
| _internalEventId  | GUID  | ADD DESCRIPTION  |
| isPremium  |  boolean | Whether the Wix site is a Premium site. |  
| userId | GUID  | Wix user ID |  
| metaSiteId  | GUID  | Wix site ID |

### Example

```json
{
  "origin": "Stores",
  "id": "362b1084-060a-49d8-9ba3-e4701d2dac32",
  "name": "Coffee Extravaganza: Four 250g Blends of Premium Beans",
  "price": 67.5,
  "currency": "USD",
  "quantity": 1,
  "sku": "",
  "type": "physical",
  "brand": null,
  "checkoutId": "8bdbb122-4542-4b70-a9dd-05cc71214b00",
  "contents": [
    {
      "id": "362b1084-060a-49d8-9ba3-e4701d2dac32",
      "name": "Coffee Extravaganza: Four 250g Blends of Premium Beans",
      "price": 67.5,
      "currency": "USD",
      "quantity": 1
    }
  ],
  "visitorId": "6d0465bd-ea9e-4fdf-b7f4-6979755e13d8",
  "_internalEventId": "812c63ad-8d51-4ec2-8ba0-5bb7555e45a9",
  "isPremium": true,
  "userId": "31ff72a7-bc9f-4925-bc84-e0d2fe493a5a",
  "metaSiteId": "9b7f4f1c-f125-4a36-92a7-9eb1e0f0fbf6"
}
```
