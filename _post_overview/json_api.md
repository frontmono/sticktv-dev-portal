---
title: JSON API
position: 1
right_code: |
    **Service Login**
    ``` 
    http://api.stick.tv/gr_login?jver=2&gr_nm=singlab&gr_key=f7d2d2599d49dd6c755a62314185d98b
    ``` 
    
---

Applications that interface directly with the **{{site.data.const.names.service}}** will need interact with RESTful API.

### Public Domain

|Domain|Status|
|---|---|
|api.stick.tv|Production Server|
|api.dev.stick.tv|Test Server|

##### Service Login API
+ **uri:**  gr_login
+ **param(GET)**
    + **jver:** api version
    + **gr_nm:** app group name
    + **gr_key:** service key
    

##### Content List API
*TODO*

