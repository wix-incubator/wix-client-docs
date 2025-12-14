# Page View

<blockquote class="warning">

**Deprecation Warning:** 

The client-side analytics events documented in this reference are deprecated. All event documentation has been moved to the SDK and is now available through the [Analytics API](https://dev.wix.com/docs/sdk/host-modules/site/analytics/introduction). 

</blockquote>

Triggered whenever a site page is opened.

**Properties**:

|Name|Type|Description|  
|---|---|---|  
|pageId|text|Page ID|
|pageNumber|number|Page number|
|pagePath|text|Page path|
|pageTitle|text|Page title|
|isPremium|boolean|Whether the Wix site is Premium|  
|userId|text|User ID|  
|metaSiteId|text|Wix site ID|

**Example**:
```JSON
{
    "isPremium": true,
    "metaSiteId": "e4d85293-d205-48d0-93d4-3ed7b91b9549",
    "pageId": "c1dmp",
    "pageNumber": 4,
    "pagePath": "",
    "pageTitle": "Headphones LP",
    "userId": "79f246a8-46fd-4429-aac6-006d13cce9a6"
}
```
