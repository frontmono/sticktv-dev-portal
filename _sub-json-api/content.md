---
title: Content Related API
position: 1
layout: full-page
---
- [Content List(External)](#content-list-sns)
- [Content List(Moment)](#content-list-home)


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


# content-list-home

content list in Monent

+ **uri:**  *https://{domain}/{version}/list/content/home*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|gr_idx|NO|group idx, default: logined group idx |
|user_idx|NO|default: logined user idx|
|type|YES|group: group's timeline, user: group/user's timeline, own: logined user's timeline, user login required|
|page|NO|default: 1|
|count|NO|default: 5|

+ **Result**

> Data Result. Json Array. Same as sns content list but, meta is different
>
|name|type|note|
|---|---|-|
|file_type|String|Video/Text/Audio/Photo|
|status|String|A: active, S: transcoding|
|publishedAt|String|uploaded datetime|
|user_idx|String|owner user idx|
|user_thumb|String|owner user thumbnail|
|user_nickname|String|owner user nickname|
|demension|String|{width}x{height}. if thumbnail specified|
|play_url|String|photo?: image url, video/audio? hls/mp3 url|
|duration|String|in seconds when video/audio|




+ **example**

> https://dev.api.stick.tv:8301/1.0.0/list/content/home

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

