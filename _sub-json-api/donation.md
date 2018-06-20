---
title: Donation Related API
position: 1
layout: full-page
---

- [Braintree Client Token](#braintree-client-token)
- [Braintree Checkout](#braintree-charge-point)
- [Charging History](#point-charge-history)
- [Give to Content](#point-give-content)
- [Content Give History](#content-give-history)

# braintree-client-token

check on  https://developers.braintreepayments.com/guides/drop-in/setup-and-integration/ios/v4


+ **uri:**  *https://{domain}/{version}/braintree/clientToken*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|unit|YES|100 / 500 / 1000 :  point|
|amount|YES|US Dollar. ex: 0.99|
|nonce|YES|Drop in UI's nonce result|

**Result**

>
|name|type|note|
|---|---|-|
|token|String|-/-|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/braintree/clientToken

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# braintree-charge-point
charge point with credit card information

+ **uri:**  *https://{domain}/{version}/braintree/checkout*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-/-|

**Result**
> Result have transaction & balance

# result-transaction

>
|name|type|note|
|---|---|-|
|idx|String|transaction idx|
|price|String|us dollar price|
|count|String|charged point count|
|date|String|transaction date|
|type|String|purchased|

# result-balance

>
|name|type|note|
|---|---|-|
|purchased|String|purchased balance|
|earned|String|earned balance|


+ **example**

N/A

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# point-charge-history
return list of charge transaction
+ **uri:**  *https://{domain}/{version}/heart/chargeHistory*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|page|NO|-/-|
|count|NO|-/-|

**Result**

list of transaction. [refer](#result-transaction)

+ **example**

N/A

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

# point-give-content
Send heart to content owner

+ **uri:**  *https://{domain}/{version}/heart/give/content*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|cid|YES|content id|
|point|YES|point will be credited to content owner|

**Result**

> 
|name|type|note|
|---|---|-|
|content|String|total point of content. new balance of content|
|balance|Dictionary|new balance of user. [refer](#result-balance)|


+ **example**

N/A

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

# content-give-history
List of donation transaction for content

+ **uri:**  *https://{domain}/{version}/heart/give/content/history*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|cid|YES|content id|
|page|NO|-/-|
|count|NO|-/-|

**Result**

> 
|name|type|note|
|---|---|-|
|idx|String|donation tranaction idx|
|point|String|Donated point|
|user/idx|String|user idx|
|user/thumb|String|user thumb|
|user/nickname|String|user nickname|


+ **example**

N/A

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


--