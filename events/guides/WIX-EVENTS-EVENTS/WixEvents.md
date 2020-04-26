# Widget View (Event Widget/Gallery)

Triggered whenever a page is loaded that contains either an event gallery or widget.

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|text|Event name |
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|contents|array|All  events |
|contents.name|text|Event name|
|contents.list|text|Name of relevant event gallery/widget|
|position|number|Event position in the gallery/widget|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
    "event": "widgetView",
    "eventLabel": "Wix Events",
    "eventCategory" : "Enhanced Ecommerce",
    "contents": [ {
      "name": "Some great event",
      "list": "Widget",
    "position": 1
  }, 
  {
    "name": "Some bad event",
    "list": "Widget",
    "position": 2
  } ]
} );
```

# Click Product

Triggered when the user clicks on a event from any of the galleries.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|name|text|event name |
list|text|Name of relevant event gallery|
|position|number|Event position in the gallery|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("ClickProduct", {
  "origin": "Wix Events",
  "name": "Some bad event",
    "list": "Widget",
    "position": 2
} );
```

# Add To Cart

Triggered when user adds a ticket to the cart.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|name|text|event name |
|price|number|The price of the ticket|
|currency|currency|Currency in ISO-4217 format|
|variant|text|ticket type|
|position|number|Event position in the gallery|
|quantity|number|Number of tickets added|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("AddToCart", {
  "origin": "Wix Events",
  "name": "Some bad event",
  "price": 130,
  "currency": "USD",
  "variant": "regular",
  "position": 2,
  "quantity": 1 
} );
```

# Remove From Cart

Triggered when the user clicks to remove a ticket from the cart.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|name|text|Event name |
|price|number|Ticket price|
|currency|currency|Currency in ISO-4217 format|
|variant|text|Ticket type|
|position|number|Event position in the gallery|
|quantity|number|Number of tickets added|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("RemoveFromCart", {
  "origin": "Wix Events",
  "name": "Some bad event",
  "price": 130,
  "currency": "USD",
  "variant": "regular",
  "position": 2,
  "quantity": 1 
} );
```

# Add Assigned

Triggered when the more than 1 ticket is selected.

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|test|event name|
|eventCategory|text|Wix category|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "AddAssigned",
    "eventLabel": "Wix Events",
    "eventCategory" : "Enhanced Ecommerce"
} );
```

# Add Coupon

Triggered when the user adds a coupon.

**Properties**:
|Name|Type|Description|
|---|---|---|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "AddCoupon",
    "eventLabel": "Wix Events",
   "eventCategory": "Enhanced Ecommerce",
} );
```

# Initiate Checkout

Triggered when the ‘Checkout’ button is clicked.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Bookings |
|contents|array|All events in cart |
|contents.name|text|Event name|
|contents.price|number|Ticket price|
|contents.currency|currency|Currency in ISO-4217 format|
|contents.variant|text|Ticket type|
|contents.quantity|number|Number of tickets|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("InitiateCheckout", {
  "origin": "Wix Events",
  "contents": [ {
    "name": "Some bad event",
  "price": 130,
  "currency": "USD",
  "variant": "regular", 
  "quantity": 4  
  }, {
    "name": "Some great event",
  "price": 180,
  "currency": "USD",
  "variant": "vip", 
  "position": 2,
  "quantity": 2  
  } ]
} );
```
# Add Payment Info

Triggered after the user adds their payment information.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Stores, Bookings|
|option|text|Additional information to send with Extended Ecommerce checkout step|

**Example**:
```JSON
trackEvent("AddPaymentInfo", {
  "origin": "Wix Events",
  "option": "Paypal"
} );
```

# Purchase

Triggered on thank-you-page load.

**Properties**:
|Name|Type|Description|
|---|---|---|
|origin|text|Wix App name, i.e Events, Stores|
|revenue|number|Total purchase amount|
|tax|number|Purchase tax|
|coupon|text|Coupon name|
|contents|array|All purchased products/events|
|contents.quantity|number|Number of tickets|
|contents.price|number|Product/event price|
|contents.currency|currency|Currency in ISO-4217 format|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|


**Example**:
```JSON
trackEvent("Purchase", {
  "origin": "Wix Events",
  "revenue": 880,
  "tax": 20,
  "coupon": "SUMMER2018",
  "contents": [ {
    "quantity": 2,
    "price": 180,
    "currency": "USD"
  }, 
  {
    "quantity": 4,
    "price": 130,
    "currency": "USD"
  } ]
} );
```

# Track Events - RSVP FLOW 
# RSVP Click

Triggered when the user clicks "Register now".

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|text|Event name|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "Name:rsvpClick",
  "eventLabel": "Wix Events",
  "eventCategory" : "Enhanced Ecommerce"
} );
```

# RSVP Content View

Triggered when the user views RSVP content.

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|text|Event name|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "Name:RsvpContentView",
  "eventLabel": "Wix Events",
  "eventCategory" : "Enhanced Ecommerce"
} );
```

# RSVP Register Next

Triggered when the user continues registration.

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|text|Event name|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  "event": "Name:RsvpRegisterNext",
  "eventLabel": "Wix Events",
  "eventCategory" : "Enhanced Ecommerce"
} );
```

# RSVP Submit

Triggered when the user clicks submit.

**Properties**:
|Name|Type|Description|
|---|---|---|
|event|text|Event name|
|eventLabel|text|Wix App name, i.e Events, Bookings|
|eventCategory|text|Wix category|
|isPremium|boolean|Whether the Wix site is Premium|
|userId|text|User ID|
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
trackEvent("CustomEvent", {
  event: "Name:"RsvpSubmit",
  "eventLabel": "Wix Events",
  "eventCategory" : "Enhanced Ecommerce"
} );
