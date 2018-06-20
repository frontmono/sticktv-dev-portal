---
title: Fandom (Group) Related API
position: 1
layout: full-page
---

- [Comment Add](#comment-add)
- [Comment List](#comment-list)
- [Comment Add](#comment-remove)
- [Like / Unlike](#like-unlike)


# comment-add
Add comment to sepcific content

+ **uri:**  *https://{domain}/{version}/comment/add*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|cid|YES|Content Index|
|comment|YES|Comment String|

**Result**
>
|name|type|note|
|---|---|-|
|cmt_idx|String|comment idx|
|count|String|total comment count of content. normaly + 1 to previouse count|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/comment/add?cid=1&comment=hello

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

# comment-list
Show the list of comment

+ **uri:**  *https://{domain}/{version}/comment/list*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|cid|YES|Content Index|
|page|NO|-/-|
|count|NO|-/-|

**Result**
>
data include {total} and {list}. below table shows comment info
>
|name|type|note|
|---|---|-|
|idx|String|comment idx|
|comment|String|Comment String|
|user/idx|String|user idx|
|user/thumb|String|user thumbnail. |
|user/nickname|String|User's nickname |

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/comment/list?cid=1

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# comment-remove
remove comment. only can be excuted by writter.

+ **uri:**  *https://{domain}/{version}/comment/remove*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|cmt_idx|YES|Comment Index|

**Result**
>
|name|type|note|
|---|---|-|
|cmt_idx|String|removed comment idx|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/comment/remove?cmt_idx=1

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|


# like-unlike
Content Like / Unlike

+ **uri:**  *https://{domain}/{version}/like/action*
+ **method:** GET
+ **parameters**

>
|name|required|node|
|---|---|-|
|cid|YES|Content Index|
|type|YES|add or remove|

**Result**
>
|name|type|note|
|---|---|-|
|like_idx|String|Like history idx|
|count|String|total count of like in content|

+ **example**

> https://dev.api.stick.tv:8301/1.0.0/like/action?cid=1&type=add

+ **version history**

> 
|version|node|
|---|---|
|1.0.0|draft|

--