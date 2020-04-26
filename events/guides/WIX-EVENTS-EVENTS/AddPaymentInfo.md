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
