---
title: Account Related API
position: 1
layout: full-page
---
{% assign page.section = "JSON Account API " %}
- [Service Login](#service-login)
- [Session Status](#session-status)
- [User Login](#user-login)
- [User Logout](#user-logout)

# service-login
+ **uri:**  *https://{domain}/{version}/account/serviceLogin*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|name|YES|service name|
|key|YES|service key|

**Result**
>
|name|type|note|
|---|---|-|
|token|String|must be set in GET or Cookie as [SSID] paramter name|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/serviceLogin?name=wetribe&key=01e13abd92441b59ed8caae67c768c77f527ec71d5e7b28487c5056a9610ba4e

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

# session-status
+ **uri:**  *https://{domain}/{version}/account/status*
+ **method:** GET
+ **parameters** N/A

**Result**
>
|name|type|note|
|---|---|-|
|token|String|must be set in GET or Cookie as [SSID] paramter name|
|info|Dictionary|session status information|

>>
info dictionary structure
>>
|name|type|note|
|---|---|-|
|prefix|String|same as service name [Service Login](#service-login)|
|gr_idx|String or Boolean|current selected tribe idx|
|usr_idx|String or Boolean|current loggined user idx|
|usr_email|String or Boolean|current loggined user email|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/status

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

# user-login
+ **uri:**  *https://{domain}/{version}/account/userLogin*
+ **method:** GET 
+ **parameters**

>
|name|required|node|
|---|---|-|
|uid|YES|user name|
|pass|YES|passcode|

**Result**
>
|name|type|note|
|---|---|-|
|user_idx|String| as digit number|
|user_email|String| user email |


+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/userLogin?uid=hskim&pass=a1234

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# user-logout
+ **uri:**  *https://{domain}/{version}/account/userLogout*
+ **method:** GET 
+ **parameters** N/A

**Result**
>
|name|type|note|
|---|---|-|
|user_idx|String| previous logined user idx or "none" if not exist|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/userLogout

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

-

