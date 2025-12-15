## Initiate Checkout

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered when the 'Book Now' button is clicked.

**Properties**:

| Name                | Type     | Description                              |
|---------------------|----------|------------------------------------------|
| **contents**        | Array    | All products in cart                     |
| contents.**Id**     | text     | Product ID                               |
| contents.**name**   | text     | Product Name                             |
| contents.**brand**  | text     | Business Name                            |
| contents.**category**| text    | Collection Name                          |
| contents.**variant**| text     | Selected choice from 1st product option  |
| contents.**price**  | currency | Product price                            |
| contents.**currency**| currency | default site currency in ISO-4217 format |
| contents.**quantity**| integer  | Quantity of product added to cart        |
| contents.**dimension1**| text   | XXX                                      |
| contents.**dimension2**| text   | XXX                                      |
| **origin**          | text     | Wix App name, i.e Stores, Bookings       |
| **isPremium**       | boolean  | Whether the Wix site is Premium          |
| **userId**          | text     | User ID                                  |
| **metaSiteId**      | text     | Wix site ID                              |

**Example**:
```JSON
{
    "contents": [{
        "brand": "",
        "category": "",
        "currency": undefined,
        "id": "8811abeb-58dc-4596-b731-174980819aaa"
        "name": undefined,
        "price": undefined,
        "variant": "PRIVATE",
        "length": 1,
        "isPremium": true,
        "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549",
        "origin": "Bookings",
        "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6"
    }]
}
```

## CustomEvent - Select Date

```JSON
{
    "contents": [{
        "id": "8811abeb-58dc-4596-b731-174980819aaa", 
        "name": "test 1-on-1", 
        "category": "", 
        "variant": "PRIVATE", 
        "price": 150, 
        "..."
    }],
    "length": 1,
    "eventAction": "Select Date",
    "eventCategory": "Enhanced Ecommerce - Bookings",
    "isPremium": true,
    "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549",
    "origin": "Bookings",
    "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6"
}
```

## StartPayment
