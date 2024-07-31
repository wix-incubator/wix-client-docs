# View Content

Triggered when a visitor views the product page.

## View Content: Event Properties

| Name                          | Type             | Description                                                                                                                                                                                                                                                                                                                                                                                                |
| ----------------------------- | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| origin                        | string           | Wix App that emitted this event, such as "Stores" or "Bookings."                                                                                                                                                                                                                                                                                                                                         |
| id                            | GUID             | Product ID.                                                                                                                                                                                                                                                                                                                                                                                              |
| name                          | string           | Product name.                                                                                                                                                                                                                                                                                                                                                                                            |
| price                         | number           | Product price.                                                                                                                                                                                                                                                                                                                                                                                           |
| currency                      | currency         | Default site currency in ISO-4217 format.                                                                                                                                                                                                                                                                                                                                                                |
| sku                           | string           | Product Stock Keeping Unit (SKU).                                                                                                                                                                                                                                                                                                                                                                        |
| type                          | string           | Product type. Possible values are `physical` and `digital`.                                                                                                                                                                                                                                                                                                                                              |
| brand                         | string           | Product brand.                                                                                                                                                                                                                                                                                                                                                                                           |
| dimension3                    | string           | Custom Google Analytics dimension defined for this product. Learn more about [custom dimensions & metrics](https://support.google.com/analytics/answer/2709828#zippy=%2Cin-this-article) in Google Analytics.                                                                                                                                                                                            |
| variants                      | array of objects | Optional. Product variants.                                                                                                                                                                                                                                                                                                                                                                              |
| variants.id                   | GUID             | Variant ID. Learn more about [product options and variants](https://support.wix.com/en/article/wix-stores-adding-and-customizing-product-options).                                                                                                                                                                                                                                                       |
| variants.optionsSelectionsIds | array of numbers | Optional. User selections of product options, such as size or color, listed in the order they appear on the site dashboard. For example, the array `[2,0,2]` indicates choice 3 for the first option, choice 1 for the second option, and choice 3 for the third. Learn more about [product options and variants](https://support.wix.com/en/article/wix-stores-adding-and-customizing-product-options). |
| variants.price                | number           | Variant price.                                                                                                                                                                                                                                                                                                                                                                                           |
| variants.sku                  | string           | Variant Stock Keeping Unit (SKU) ID.                                                                                                                                                                                                                                                                                                                                                                     |
| options                       | array of objects | Product options, such as size or colors.                                                                                                                                                                                                                                                                                                                                                                 |
| visitorId                     | GUID             | Site visitor ID.                                                                                                                                                                                                                                                                                                                                                                                         |
| \_internalEventId             | GUID             | Event ID.                                                                                                                                                                                                                                                                                                                                                                                                |
| isPremium                     | boolean          | Whether the Wix site is a Premium site.                                                                                                                                                                                                                                                                                                                                                                  |
| userId                        | GUID             | Wix user ID.                                                                                                                                                                                                                                                                                                                                                                                             |
| metaSiteId                    | GUID             | Wix site ID.                                                                                                                                                                                                                                                                                                                                                                                             |

### Example

```json
{
  "origin": "Stores",
  "id": "bc749422-649a-14e1-c81d-6cee619ba944",
  "name": "Athena: Ouzo of the Gods",
  "price": 55,
  "currency": "USD",
  "sku": "",
  "type": "physical",
  "brand": null,
  "dimension3": "in-stock",
  "variants": [
    {
      "id": "0ec85795-ac0c-4f91-8584-4ba0a1c43359",
      "optionsSelectionsIds": [1, 5],
      "price": 50,
      "sku": "1212121"
    },
    {
      "id": "8e093c14-7f29-4252-876c-a5677293b9ed",
      "optionsSelectionsIds": [1, 6],
      "price": 52,
      "sku": ""
    },
    {
      "id": "bb433bea-10ec-4063-88b0-58c3cbfd4044",
      "optionsSelectionsIds": [1, 7],
      "price": 80,
      "sku": ""
    }
  ],
  "options": [
    {
      "id": 1,
      "value": "60 ml"
    },
    {
      "id": 2,
      "value": "200 ml"
    },
    {
      "id": 3,
      "value": "500 ml"
    },
    {
      "id": 4,
      "value": "750 ml"
    }
  ],
  "visitorId": "6d0465bd-ea9e-4fdf-b7f4-6979755e13d8",
  "_internalEventId": "bbdb1769-39c0-48d3-9a5c-0f822d75b0ab",
  "isPremium": true,
  "userId": "31ff72a7-bc9f-4925-bc84-e0d2fe493a5a",
  "metaSiteId": "9b7f4f1c-f125-4a36-92a7-9eb1e0f0fbf6"
}
```
