# Wix Stores Events

## Add Product Impression

Triggered when a page is loaded that contains a product gallery or widget.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|contents|array|All purchased products |  
|contents.id|text|Product ID|
|contents.name|text|Product name|
|contents.list|text|Name of relevant product gallery|
|contents.category|text|Collection name|
|contents.position|number|Product position in the gallery|
|contents.price|currency|Product price|
|contents.currency|currency|Default site currency in ISO-4217 format|
|origin|text|Wix App name, i.e Stores, Bookings |  
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:  
```JSON
{
  "contents": [{
    "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e", 
    "name": "Shoes", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 0, 
    "price": 85,
    "currency": "USD"
  },
  {
    "id": "cd59cd36-b6d2-2cf3-9d48-81793a7bdbbd", 
    "name": "Reading glasses", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 1,
    "price": 20,
    "currency": "USD"
  },
  {
    "id": "c8539b66-7a44-fe18-affc-afec4be8562a", 
    "name": "Watch", 
    "list": "Grid Gallery", 
    "category": "All Products", 
    "position": 2,
    "price": 10,
    "currency": "USD"
  }],
  "origin": "Stores", 
  "isPremium": true, 
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661", 
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```

## Click Product

Triggered when the user clicks on a product from any of the galleries.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|id|text|Product ID|
|origin|text|Wix App name, i.e Stores, Bookings |
|name|text|Product Name|
|list|text|Name of relevant product gallery|
|category|text|Collection Name|
|position|integer|Product position in the gallery|
|price|currency|Product Price|
|currency|currency|default site currency in ISO-4217 format|
|sku|text|Product SKU|
|type|text|Product type: physical or digital|
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
  "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e",
  "origin": "Stores",
  "name": "Shoes",
  "list": "Grid Gallery",
  "category": "All Products",
  "position": 1,
  "price": 85,
  "currency": "USD",
  "type": "physical",
  "sku": "364215376135191",
  "isPremium": true,
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661",
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```

## Product Page Loaded

Triggered whenever a product page loads.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|id|text|Product ID|
|name|text|Product Name|
|price|currency|Product Price|
|currency|currency|default site currency in ISO-4217 format|
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
"productId":"8fe8f05f-951e-1563-b917-88adf8284543",
"name":"I'm a Product",
"currency":"ILS",
"price":200,
"isPremium":true,
"userId":"1c9b561f-0093-4eea-ac65-4278ba023678",
"metaSiteId":"999514f5-6fb1-457a-8d0d-a67d01841abd"
}
```


## Add to Cart

Triggered when user clicks on the ‘Add to cart’ button.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|category|text|Collection Name|
|origin|text|Wix App name, i.e stores, bookings |
|id|text|Product ID|
|name|text|Product Name|
|variant|text|Selected choice from 1st product option|
|price|currency|Product price|
|currency|currency|default site currency in ISO-4217 format|
|quantity|integer|Quantity of product added to cart|
|sku|text|Product SKU|
|type|text|Product type: physical or digital|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metasiteId|text|Wix site ID|

**Example**:
```JSON
{
  "category": "All Products",
  "origin": "Stores",
  "id": "cd59cd36-b6d2-2cf3-9d48-81793a7bdbbd",
  "name": "Reading glasses",
  "price": 20,
  "currency": "USD",
  "quantity": 1,
  "sku": "364215375135191",
  "type": "physical",
  "isPremium": true,
  "userId": "affea1e3-8652-4b59-a3a0-e8f88fdab661",
  "metaSiteId": "58617836-3714-4dac-860a-dd524531c13e"
}
```


## Remove from Cart

Triggered when the user clicks to remove an item from the cart.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e stores, bookings |
|id|text|Product ID|
|name|text|Product Name|
|category|text|Collection Name|
|variant|text|Selected choice from 1st product option|
|price|currency|Product price|
|currency|currency|default site currency in ISO-4217 format|
|quantity|integer|Quantity of product added to cart|
|sku|text|Product SKU|
|type|text|Product type: physical or digital|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
   "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e",
   "origin": "Stores",
   "name": "Soundbeam ERD - 3083",
   "category": "All Products",
   "currency": "ILS",
   "price": 220,
   "quantity": 2,
   "sku": "00001",
   "type": "physical",
   "isPremium": true,
   "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
   "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"    
}
```


## Initiate Checkout

Triggered when the ‘Checkout’ button is clicked.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|contents|Array|All products in cart|  
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|contents.category|text|Collection Name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product price|
|contents.currency|currency|default site currency in ISO-4217 format|
|contents.quantity|integer|Quantity of product added to cart|
|origin|Text|Wix App name, i.e Stores, Bookings |  
|isPremium|Boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
 "contents": [{
    "id": "df19c1f7-07d8-a265-42f8-e8dfa824cc6e", 
    "name": "Soundbeam ERD - 3083", 
    "category": "All Products", 
    "price": 220, 
    "currency": "ILS", 
    "quantity": 1
  }],
  "length": 1,
  "origin": "Stores",
  "isPremium": true,
  "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6",
  "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549"
}
```


## Start Payment

Triggered when the user gets to the payment part of the checkout funnel.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e Stores, Bookings |
|contents|Array|All products in cart|  
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|contents.category|text|Collection Name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product Price|
|contents.currency|currency|default site currency in ISO-4217 format|


**Example**:
```JSON
trackEvent("StartPayment", 
  {
    "origin": "Stores",
    "option": "Express",
    "contents": [{
      "id": "T123", 
      "name": "Running shoes",
      "..."
    }]
  }
```

## Add Payment Info

Triggered after the user adds their payment information.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|origin|text|Wix App name, i.e Stores, Bookings |
|option|text|Additional information to send with Extended Ecommerce checkout step|
|contents|Array|All products in cart|  
|contents.Id|text|Product ID|
|contents.name|text|Product Name|
|contents.category|text|Collection Name|
|contents.variant|text|Selected choice from 1st product option|
|contents.price|currency|Product Price|
|contents.currency|currency|default site currency in ISO-4217 format|

**Example**:

```JSON
{
  "origin": "Stores",
  "option": "Express",
  "contents": [{
    "id": "T123", 
    "name": "Running shoes",
    "..."
  }]
}
```

## Purchase

Triggered on thank-you-page load.


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
