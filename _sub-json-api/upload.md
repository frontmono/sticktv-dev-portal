---
title: Content Related API
position: 1
layout: full-page
---
- [Any File Upload](#simple-file-upload)
- [Content Add ](#content-add)


# simple-file-upload


+ **uri:**  *https://{domain}/{version}/upload/file*
+ **method:** POST
+ **parameters**. User Login Required

>
|name|required|node|
|---|---|-|
|type|YES|image/video/audio/dummy|
|file|YES|attached name|

**Result**

> Data Result
> 
|name|type|note|
|---|---|-|
|url|String|Uploaded URL|
|amount|String|uploaded file size. if it has thumbnail, added thumb file size to original|
|key|String|used to content at [at](#content-add) |


+ **example**

> N/A

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# content-add

add upload data to my content (kind of upload)

+ **uri:**  *https://{domain}/{version}/upload/addContent*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|title|NO|content title |
|desc|NO|content description|
|gr_idx|NO|target fandom idx|
|page|NO|default: 1|
|count|NO|default: 5|

+ **Result**

> Data Result. Json Array. Same as sns content list but, meta is different
>
|name|type|note|
|---|---|-|
|cid|String|Uploaded content idx|



+ **example**

> N/A

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

