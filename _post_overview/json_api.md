---
title: JSON API
position: 1
right_code: |
    **Service Login**
    ``` 
    https://dev.api.stick.tv/api/1.0.0/gr_login?gr_nm=stick_developer&gr_key=a5204a2e9f78f8b5ab85b0d510b506e6
    ``` 
    
    
    **Service Login**
    ``` 
    http://dev.api.stick.tv/api/1.0.0/gr_content_list?page=1&count=3
    ``` 
        
---

Applications that interface directly with the **{{site.data.const.names.service}}** will need interact with RESTful API.

### Public Domain

|Domain|Status|
|---|---|
|api.stick.tv|Production Server|
|api.dev.stick.tv|Test Server|

##### Service Login API
+ **uri:**  https://{domain}/api/{version}/gr_login
+ **param(GET)**
    + **gr_nm**(require): app group name
    + **gr_key**(require): service key
    

##### Content List API
+ **uri:**  https://{domain}/api/{version}/gr_content_list
+ **param(GET)**
    + **page**(optional): result paging. start from 1
    + **gr_key**(optional): once result count. (1 - 200)

