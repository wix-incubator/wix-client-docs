# Add to Cart

Triggered when user clicks on the **Add to cart** button.

## Add to Cart: Event Properties

| Name              | Type     | Description                                                      |
| ----------------- | -------- | ---------------------------------------------------------------- |
| origin            | string   | Wix App that emitted this event, such as "Stores" or "Bookings." |
| id                | GUID     | Product ID.                                                      |
| name              | string   | Product name.                                                    |
| price             | number   | Product price.                                                   |
| currency          | currency | Default site currency in ISO-4217 format.                        |
| quantity          | number   | Product quantity.                                                |
| sku               | string   | Product Stock Keeping Unit (SKU).                                |
| type              | string   | Product type. Possible values are `physical` and `digital`.      |
| brand             | string   | Product brand.                                                   |
| visitorId         | GUID     | Site visitor ID.                                                 |
| _internalEventId | GUID     | Event ID.                                                        |
| isPremium         | boolean  | Whether the Wix site is a Premium site.                          |
| userId            | GUID     | Wix user ID.                                                     |
| metaSiteId        | GUID     | Wix site ID.                                                     |

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
  "visitorId": "6d0465bd-ea9e-4fdf-b7f4-6979755e13d8",
  "_internalEventId": "905bc987-0681-4148-93b0-b0d255b48d83",
  "isPremium": true,
  "userId": "31ff72a7-bc9f-4925-bc84-e0d2fe493a5a",
  "metaSiteId": "9b7f4f1c-f125-4a36-92a7-9eb1e0f0fbf6"
}
```
