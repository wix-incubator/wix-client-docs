# Product Page Loaded

Triggered whenever a product page loads.

## Product Page Loaded: Event Properties

| Name |  Type  | Description |
| --- | --- | --- |
| productId | GUID  | Product ID  |
| name  | string  | Product name  |
| currency  | currency  | Default site currency in ISO-4217 format  |
| price  | number | Product price |
| sku  | string  | Product Stock Keeping Unit (SKU)  |
| visitorId  |  GUID | Site visitor ID |
| _internalEventId  | GUID | ADD DESCRIPTION  |
| isPremium  |  boolean | Whether the Wix site is a Premium site. |  
| userId | GUID  | Wix user ID |  
| metaSiteId  | GUID  | Wix site ID |

### Example

```json
{
  "productId": "224c5d1b-e278-06d1-dea5-ec51528d266a",
  "name": "Utokia Hemp CBD Pre-Roll 6 Joint Adventure Pack",
  "currency": "USD",
  "price": 29,
  "sku": "",
  "visitorId": "6d0465bd-ea9e-4fdf-b7f4-6979755e13d8",
  "_internalEventId": "2206e562-b643-40bd-87c2-657e3bceac0f",
  "isPremium": true,
  "userId": "31ff72a7-bc9f-4925-bc84-e0d2fe493a5a",
  "metaSiteId": "9b7f4f1c-f125-4a36-92a7-9eb1e0f0fbf6"
}
```
