---
title: Account Related API
position: 1
layout: full-page
---
{% assign page.section = "JSON Account API " %}
- [Service Login](#service-login)


# service-login
+ **uri:**  *https://{domain}/api/{version}/gr_login*
+ **method:** GET or POST 
+ **parameters**

>
|name|required|node|
|---|---|-|
|gr_nm|YES|app group name|
|gr_key|YES|service key|

+ **example**

> https://dev.api.stick.tv/api/1.0.0/gr_login?gr_nm=stick_developer&gr_key=a5204a2e9f78f8b5ab85b0d510b506e6

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

