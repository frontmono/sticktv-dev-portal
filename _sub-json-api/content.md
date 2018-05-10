---
title: Content Related API
position: 1
layout: full-page
---
- [Content List(External)](#content-list-sns)

# content-list-sns
content list from youtube, faceboo, etc

+ **uri:**  *https://{domain}/{version}/list/content/sns*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|ch_idx|YES|target channel idx|
|count|NO|default: 5|
|nextToken|NO|specify next page token|

**Result**

> Data Result
> 
|name|type|note|
|---|---|-|
|type|String|YouTube/etc|
|items|array|explain next paragraph|
|nextToken|String|next page token|

> items information. meta area can be different in sns service type.
> 
|name|type|note|
|---|---|-|
|cid|String|must be 0. because content from other SNS service|
|title|String|-/-|
|description|String|-/-|
|thumbnail|String|-/-|
|ukey|String|unique key to distinguish in all list result|
|meta|Dictionary|other meta values different in each service|

> Youtube Meta
>
|videoID|String|youtube video ID|
|channelId|String|youtube channel ID|
|publishedAt|String|youtube created date|


+ **example**

> https://dev.api.stick.tv:8301/1.0.0/list/content/sns

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

