---
title: Assignment 4
layout: doc
---


## Abstract Data Models

[link to A3](assignment3.html)

#### Posting
author: User -> one String  
time: Post -> one Date  
title: Post -> one String  
creator: Post -> one String  
rating: Item -> Integer  
label: Item -> set Labels  
Labels: enum("movie", "book", "album", "TV show", "other")  



#### Commenting [Item]
author: User -> one String  
time: one Date  
content: one String  


#### Recommending [User]
recommendations: set Recommendation  
from: recommendations -> User  
content: set Item  
recommendation: User -> one Item



#### Friending [User]
friends: User -> set User



#### Authenticating
registered: set User  
username, password: registered -> one String  



#### Sessioning [User]
active: set Session  
user: active -> one User




## Backend Code Repository and Deployment Links

[Backend Code](https://github.com/BouncyBabylons/a4_backend_starter)

[Deployment Link](https://enny.vercel.app/)  