# Customize Product

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when a user changes something on the product page, such as choosing the product size or color.

## Customize Product: Event Properties

| Name                 | Type             | Description                                                                                                                                                                                                                                                                                                                                                                                              |
| -------------------- | ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| origin               | string           | Wix App that emitted this event, such as "Stores" or "Bookings."                                                                                                                                                                                                                                                                                                                                         |
| id                   | GUID             | Product ID.                                                                                                                                                                                                                                                                                                                                                                                              |
| name                 | string           | Product name.                                                                                                                                                                                                                                                                                                                                                                                            |
| price                | number           | Product price.                                                                                                                                                                                                                                                                                                                                                                                           |
| currency             | currency         | Default site currency in ISO-4217 format.                                                                                                                                                                                                                                                                                                                                                                |
| quantity             | number           | product quantity.                                                                                                                                                                                                                                                                                                                                                                                        |
| sku                  | string           | Product Stock Keeping Unit (SKU).                                                                                                                                                                                                                                                                                                                                                                        |
| type                 | string           | Product type. Possible values are `physical` and `digital`.                                                                                                                                                                                                                                                                                                                                              |
| brand                | string           | Product brand.                                                                                                                                                                                                                                                                                                                                                                                           |
| variantId            | GUID             | Optional. Product variant ID. Learn more about [product options and variants](https://support.wix.com/en/article/wix-stores-adding-and-customizing-product-options).                                                                                                                                                                                                                                     |
| optionsSelectionsIds | array of numbers | Optional. User selections of product options, such as size or color, listed in the order they appear on the site dashboard. For example, the array `[2,0,2]` indicates choice 3 for the first option, choice 1 for the second option, and choice 3 for the third. Learn more about [product options and variants](https://support.wix.com/en/article/wix-stores-adding-and-customizing-product-options). |
| customTextFields     | array of strings | Optional. Values of custom text fields, such as **Gift Message**, listed in the order they appear on the page. Learn more about [custom text fields](https://support.wix.com/en/article/wix-stores-allowing-customers-to-add-a-message-when-purchasing-a-product).                                                                                                                                           |
| visitorId            | GUID             | Site visitor ID.                                                                                                                                                                                                                                                                                                                                                                                         |
| \_internalEventId    | GUID             | Event ID.                                                                                                                                                                                                                                                                                                                                                                                                |
| isPremium            | boolean          | Whether the Wix site is a Premium site.                                                                                                                                                                                                                                                                                                                                                                  |
| userId               | GUID             | Wix user ID.                                                                                                                                                                                                                                                                                                                                                                                             |
| metaSiteId           | GUID             | Wix site ID.                                                                                                                                                                                                                                                                                                                                                                                             |


### Example

```json
{
  "origin": "Stores",
  "id": "d99d3cc8-bc75-ec47-6c72-f713016f98f3",
  "name": "Taki: The Classic Card Game",
  "price": 12,
  "currency": "USD",
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
