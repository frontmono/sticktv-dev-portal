---
title: Fandom (Group) Related API
position: 1
layout: full-page
---

- [Group List](#group-list)
- [Group's Channel List](#group-category-channel)


# group-list
shows user's group(fandom) list

+ **uri:**  *https://{domain}/{version}/list/group*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|user_idx|NO|target user idx. If not specified default use logined user idx|
|range|NO|{own}: user's created group. {joined}: Joined group, {all}: own_joined, {search}: group search and require keyword|
|keyword|NO|used when range is {search} |

**Result**
>
data include {total} and {list}. below table shows group info
>
|name|type|note|
|---|---|-|
|gr_idx|String|group idx|
|logo|String|group thumbnail|
|disp_name|String|group display name|
|gr_nm|String|group unique name. |
|category|String|group category like 'fandom', 'movie', etc. |
|owner/user_idx|String|group creator user idx. |
|owner/nickname|String|group creator nickname. |

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/list/group?range=search&keyword=a

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# group-category-channel
shows channels from sepecified category in group.

+ **uri:**  *https://{domain}/{version}/list/channel/groupCategory*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|gr_idx|NO|target group idx. if not specified use default logined group|
|category|YES|pre-fixed value. {SNS/...}|


**Result** (channels)
>
|name|type|note|
|---|---|-|
|ch_idx|String|channel idx|
|thumbnail|String|channel thumbnail|
|title|String|-/-|
|type|String|{YT}:youtube channel |

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/list/channel/groupCategory?category=SNS&gr_idx=13283

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


-

