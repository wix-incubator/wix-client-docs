# Product Page Loaded

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
