---
title: JSON API
position: 1
right_code: |
    **Service Login**
    ``` 
    https://dev.api.stick.tv:8301/1.0.0/account/serviceLogin?name=wetribe&key=01e13abd92441b59ed8caae67c768c77f527ec71d5e7b28487c5056a9610ba4e
    ``` 
    
    
        
---

Applications that interface directly with the **{{site.data.const.names.service}}** will need interact with RESTful API.

### Public Domain

|Domain|Status|
|---|---|
|api.stick.tv|Production Server|
|api.dev.stick.tv:8301|Test Server|

##### ex: Service Login API
+ **uri:**  https://{domain}/{version}/account/serviceLogin
+ **param(GET)**
    + **name**(require): service name
    + **key**(require): service key
    


