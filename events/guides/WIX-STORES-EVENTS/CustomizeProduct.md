# Customize Product

Triggered whenever a user changes something on the product page, for example, choosing the product size or color.

## Customize Product: Event Properties

| Name                 | Type             | Description                                                                                                   |
| -------------------- | ---------------- | ------------------------------------------------------------------------------------------------------------- |
| origin               | string           | Wix App that emitted this event, such as "Stores" or "Bookings."                                              |
| id                   | GUID             | Product ID                                                                                                    |
| name                 | string           | Product name                                                                                                  |
| price                | number           | Product price                                                                                                 |
| currency             | currency         | Default site currency in ISO-4217 format                                                                      |
| quantity             | number           | product quantity                                                                                              |
| sku                  | string           | Product Stock Keeping Unit (SKU)                                                                              |
| type                 | string           | Product type (for example, "physical")                                                                        |
| brand                | string           | Product brand                                                                                                 |
| optionsSelectionsIds | array of numbers | Product options the user selected, such as size or color. Each array index refers to a product option.        |
| customTextFields     | array of strings | Values of custom product text fields. Each array index refers to a custom text field from page top to bottom. |
| visitorId            | GUID             | Site visitor ID                                                                                               |
| \_internalEventId    | GUID             | Event ID.                                                                                                     |
| isPremium            | boolean          | Whether the Wix site is a Premium site.                                                                       |
| userId               | GUID             | Wix user ID                                                                                                   |
| metaSiteId           | GUID             | Wix site ID                                                                                                   |

### Example

```json
{
  "origin": "Stores",
  "id": "d99d3cc8-bc75-ec47-6c72-f713016f98f3",
  "name": "Taki: The Classic Game",
  "price": 45,
  "currency": "ILS",
  "quantity": 1,
  "sku": "366615376135191",
  "type": "physical",
  "brand": null,
  "variantId": "a744cedd-7aa1-4acd-9f41-ad0588837a86",
  "optionsSelectionsIds": [3, 7],
  "customTextFields": ["Custom field 1 value", "Custom field 2 value"],
  "visitorId": "68d6bef4-f957-43fd-a7b1-9ca9ddb08b7f",
  "_internalEventId": "c161e183-6399-4527-ba26-708b5df2472c",
  "isPremium": true,
  "userId": "3b253722-5418-443d-913a-3965e451d782",
  "metaSiteId": "66274305-0db9-4138-8504-5b414ef65c97"
}
```
