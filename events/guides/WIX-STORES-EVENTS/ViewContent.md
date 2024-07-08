# View Content

Triggered whenever a visitor views their cart contents. 

## View Content: Event Properties

| Name |  Type  | Description |
| --- | --- | --- |
| origin | string  |  |
| id | GUID  | Product ID  |
| name  | string  | Product name  |
| price  | number | Product price |
| currency  | currency  | Default site currency in ISO-4217 format  |
| sku  | string  | Product Stock Keeping Unit (SKU)  |
| type  |  string | Product type (for example, "physical") |
| brand  |  string | Product brand  |
| dimension3  | string | ADD DESCRIPTION  |
| variants | array of objects | Product variants |
| variants.id | GUID | Variant ID |
| variants.optionsSelectionsIds | GUID | Product variant ID |
| variants.price | number | Product variant ID |
| variants.sku | string | Product variant Stock Keeping Unit (SKU) ID |
| visitorId  | GUID | Site visitor ID |
| _internalEventId  | GUID | ADD DESCRIPTION  |
| isPremium  |  boolean | Whether the Wix site is a Premium site. |  
| userId | GUID  | Wix user ID |  
| metaSiteId  | GUID  | Wix site ID |

### Example

```json
{
  "origin": "Stores",
  "id": "bc749422-649a-14e1-c81d-6cee619ba944",
  "name": "Coffee Bomb: Two 250g Blends of Premium Columbian Beans",
  "price": 55,
  "currency": "USD",
  "sku": "",
  "type": "physical",
  "brand": null,
  "dimension3": "in-stock",
  "variants": [
    {
      "id": "abe8c3ab-73e5-46a0-9ed7-71833d9e1d46",
      "optionsSelectionsIds": [],
      "price": 87,
      "sku": ""
    }
  ],
  "options": [],
  "visitorId": "6d0465bd-ea9e-4fdf-b7f4-6979755e13d8",
  "_internalEventId": "bbdb1769-39c0-48d3-9a5c-0f822d75b0ab",
  "isPremium": true,
  "userId": "31ff72a7-bc9f-4925-bc84-e0d2fe493a5a",
  "metaSiteId": "9b7f4f1c-f125-4a36-92a7-9eb1e0f0fbf6"
}
```
