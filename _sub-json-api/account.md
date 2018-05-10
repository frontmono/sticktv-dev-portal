---
title: Account Related API
position: 1
layout: full-page
---
{% assign page.section = "JSON Account API " %}
- [Service Login](#service-login)
- [Session Status](#session-status)
- [User Join](#user-join)
- [User Login](#user-login)
- [User Facebook Login](#user-facebook-login)
- [User Logout](#user-logout)
- [User Information](#user-information)

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

# user-join

+ **uri:**  *https://{domain}/{version}/account/userJoin*
+ **method:** GET 
+ **parameters**

>
|name|required|node|
|---|---|-|
|uid|YES|user name|
|pass|YES|passcode|
|nickname|YES| user's nickname|
|email|YES|user's email|

**Result**
>
|name|type|note|
|---|---|-|
|user_idx|String| as digit number|


+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/userJoin?uid=dev001&pass=123456&nickname=developer&email=dev001@stick.tv

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

# user-facebook-login
+ **uri:**  *https://{domain}/{version}/account/loginFacebook*
+ **method:** GET 
+ **parameters**

>
|name|required|node|
|---|---|-|
|token|YES|facebook token|

**Result**
same as [User Login](#user-login)

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/loginFacebook?token=EAADvkyB7mEEBAC1ju57G03oZAfFej9ZA4S3GGOQWFhUPGCvQrcvF90bxstnUWoQcmHWrxMAzZCFomJ91ulfR3RXEC1x3KJUksdtujPcIKFh3z8ZBiGkvF7fd1Up2ihwOtVOq8kjsIYteRc2kf1WPBXAab8YoFfKHwxWuaSD5GrFU16F1fHLmdUdSyRHDCBJGuDjiB6X7ZCZBhsOPDjw10jz2Mwv51FxMZAFjaq1TZCW4jovD0fySuE5L

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


# user-information
+ **uri:**  *https://{domain}/{version}/account/userInfo*
+ **method:** GET 
+ **parameters**

>
|name|required|node|
|---|---|-|
|user_idx|optional|user idx. If parameter not specified, use session(logined) user idx|

**Result**
>
|name|type|note|
|---|---|-|
|user_idx|String| as digit number|
|nickname|String| user email |
|thumbnail|String| user thumbnail. if want to resize image go to [Commoing Soon] |
|desc|String| user description |


+ **example**

> https://dev.api.stick.tv:8301/1.0.0/account/userLogin?uid=hskim&pass=a1234

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

