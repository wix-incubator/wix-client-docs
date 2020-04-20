# Purchase

Triggered on thank-you-page load.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|**origin**|text|Wix App name, i.e Stores, Bookings |
|**id**|text|Product ID|
|**orderId**|text|Order ID|
|**revenue**|text|Total purchase amount|
|**currency**|currency|Purchase currency in ISO-4217 format|
|**contents**|array|All purchased products|
|contents.**Id**|text|Product ID|
|contents.**name**|text|Product Name|
|contents.**category**|text|Collection Name|
|contents.**price**|currency|Product Price|
|contents.**currency**|currency|default site currency in ISO-4217 format|
|contents.**quantity**|integer|Quantity of product ordered|
|**isPremium**|Boolean|Whether the Wix site is Premium|  
|**userId**|text|User ID|  
|**metaSiteId**|text|Wix site ID|

**Example**:
```JSON
{
  "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e",
  "orderId": "d86d077c-c5d2-42c6-8b15-f5e26f276807",
  "origin": "Stores",
  "revenue": 93.6,
  "currency": "ILS",
  "contents": [{"..."}, {"..."}],
  "isPremium": true,
  "userId": "8aebf50f-b470-40b2-8376-58679347613b",
  "metaSiteId": "431559a8-b318-4176-a462-797bf50a5fad"
}
```

## Custom Events

### Shipping Details

Triggered when the user adds shipping details and clicks to advance to the next step in the checkout flow.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Fixed ‘Enhanced Ecommerce’ string(???)|
|eventAction|text|Fixed ‘Add Shipping Details’ string(???)|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent(‘CustomEvent’, 
  {
    "eventCategory": "Enhanced Ecommerce",
    "eventAction": "Add Shipping Details",
    "eventLabel": "Stores",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }],
    "isPremium": true,
    "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
    "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"
  }
```

### Delivery Method

Triggered when the user adds personal information and clicks to advance to the next step in the checkout flow.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Fixed ‘Enhanced Ecommerce’ string(???)|
|eventAction|text|Fixed ‘Add Shipping Details’ string|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", 
  {
    "eventCategory": "Enhanced Ecommerce - Stores",
    "eventAction": "Add Delivery Method",
    "eventLabel": "stores",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
  }
```

### Agree to Terms

Triggered when the user check the Agree to terms & conditions’ checkbox.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Fixed ‘Enhanced Ecommerce’ string(???)|
|eventAction|text|Fixed ‘Add Shipping Details’ string|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent(‘CustomEvent’, 
  {
    "eventCategory": "Enhanced Ecommerce",
    "eventAction": "Agree To Terms",
    "eventLabel": "Stores",
    "contents":[{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
 }
```

### Pickup Details

Triggered whenthe user enters pickup information and clicks to advance to the next step in the checkout flow.


**Properties**:

|Name|Type|Description|  
|---|---|---|  
|eventCategory|text|Fixed ‘Enhanced Ecommerce’ string(???)|
|eventAction|text|Fixed ‘Add Shipping Details’ string|
|eventLabel|text|Wix App name, i.e Stores, Bookings|
|contents|array|All purchased products|
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:

```JSON
trackEvent(‘CustomEvent’, 
  {
    "eventCategory": "Enhanced Ecommerce  - Stores",
    "eventAction": "Pickup Details",
    "eventLabel": "Stores",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
  }
```
