# Customize Product

Triggered whenever the product customization page loads.

## Customize Product: Event Properties

| Name |  Type  | Description |
| --- | --- | --- |
| origin | string  |  |
| id | GUID  | Product ID  |
| name  | string  | Product name  |
| price  | number | Product price |
| currency  | currency  | Default site currency in ISO-4217 format  |
| quantity | number | product quantity |
| sku  | string  | Product Stock Keeping Unit (SKU)  |
| type  |  string | Product type (for example, "physical") |
| brand  |  string | Product brand  |
| optionsSelectionsIds | array of numbers | ADD DESCRIPTION |
| customTextFields | array of objects | ADD DESCRIPTION |
| visitorId  | GUID | Site visitor ID |
| _internalEventId  | GUID | ADD DESCRIPTION  |
| isPremium  |  boolean | Whether the Wix site is a Premium site. |  
| userId | GUID  | Wix user ID |  
| metaSiteId  | GUID  | Wix site ID |

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
  "optionsSelectionsIds": [
    2
  ],
  "customTextFields": [],
  "visitorId": "68d6bef4-f957-43fd-a7b1-9ca9ddb08b7f",
  "_internalEventId": "c161e183-6399-4527-ba26-708b5df2472c",
  "isPremium": true,
  "userId": "3b253722-5418-443d-913a-3965e451d782",
  "metaSiteId": "66274305-0db9-4138-8504-5b414ef65c97"
}
```
