---
title: Account Related API
position: 1
layout: full-page
---
{% assign page.section = "JSON Account API " %}
- [Group Content List](#group-content-list)


# group-content-list
+ **uri:**  *https://{domain}/api/{version}/gr_content_list*
+ **method:** GET or POST 
+ **parameters**

>
|name|required|note|
|---|---|-|
|page|NO|result paging. start from 1. default: 1|
|count|NO|once result count. (1 - 200). default 30|

+ **example**

> http://dev.api.stick.tv/api/1.0.0/gr_content_list

> http://dev.api.stick.tv/api/1.0.0/gr_content_list?page=1&count=3

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

