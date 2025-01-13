# Current Member Data

<blockquote class='warning'>

**Deprecation Notice**

**This API has been replaced with the [Get Current Member](https://dev.wix.com/docs/sdk/backend-modules/members/members/get-current-member) method and will be removed on June 30, 2025. If your app uses this API, we recommend updating your code as soon as possible.**
</blockquote>

Returns information about the current site visitor (dependent on login as site member).  
Can be accessed via JavaScript on the site's client side.  
Returns a JWT with identifying details about the user/member that is signed with your public key (add link to how we sign data).  

This API should be used if your application needs to check, on the client-side, if the user is currently logged in to the site. 
In addition, it allows you to confirm this customer's identity within the insecure environment of the user's browser.


> **Important**:  
This API is dependent on the implementation of an [Embedded Script](https://dev.wix.com/docs/build-apps/develop-your-app/extensions/site-extensions/embedded-scripts/about-embedded-scripts) component, and can be accessed only via JS from the client-side browser.


### Syntax
```
GET  https://{site_domain}/_api/apps/current-member/{app_id}
```

### Request Params

|Name|Description|
|---|---|
|site_domain|Site domain|
|app_id|App ID (ensures the response will be signed with the correct key)|


### Response

|Name|Description|
|---|---|
|**member**|Member data object|
| member.**id** | GUID of the user that can be used to access more information|
|**signedToken**| A signed JWT token, which you can verify with you public key (available in the Developers Center)|
