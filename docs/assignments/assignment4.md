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




## Design Reflection

Wowee what a steep learning curve. I only feel like I began to get a feel for the frameworks, Mongo, syntax, routing procedures, and the myriad of other new technologies very recently. Rest assured, good and gracious grader, I will be further iterating upon my implementation in the coming weeks and the resulting backend will be unrivaled. For the time being, though, I will reflect on the current state of my implementation.

My commenting concept is non-traditional. I'd like Enny<sup>1</sup> and its commenting feature to have an ephemeral nature to it. I want the user's focus to be on the content other users are posting as opposed to focusing on the derivative engagement and back-and-forth that's present in other social networking apps. The way this bears out in implementation land is that comments will only be viewable by a post's author. This means there's no need to edit or delete a comment. I hesitated to include comments at all, but I'd like some way to give a virtual pat on the back, and "likes" are trite and ungenuine. 

Recommendations were another tricky concept to evaluate. On the one hand, user engagement would increase if you were to allow anybody to tag a recommendation to anybody else on any post. What if you were reading somebody's review on a documentary on golden retrievers, and your grandmother loves golden retrievers? It would make some sense to be able to recommend that documentary to her even if you'd never seen it yourself. I decided against this approach, though, and opted for quality over quantity. Users will only be able to recommend to their friends content that they have reviewed themselves i.e. the posts they've authored.

<sup>1</sup>Trademark
