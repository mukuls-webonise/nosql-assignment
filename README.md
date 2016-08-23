
NoSQL Assignment 
Users 
 
{ 
_id: “username”, 
name: “Full name here”, 
email : “​ email_here@example.com​ ”, 
password: “store pass hash here”, 
bio : “user self info”, 
teams : [ 
{ 
name: “team name”, 
role: “admin, super or editor” 
}, ... 
]  
 
} 
 
Teams  
Assumption 1 : only one admin and editor per team, otherwise would use array 
Assumption 2 : team names are unique 
{ 
_id: team name, 
admin: username, 
editor: username, 
super: username, 
users: [ username, ... ] 
} 
 
Posts 
{ 
 
author : username 
heading: “heading goes here”, 
body: “body goes here”, 
tags: [“technology”, mongoDB”, ...], images: [ {url : “image url”, alt: “image description”}, ... ], 
comments_count: 20, 
updated_at: date, 
last_comment: { embedded comment object here} 
} 
 
Comments 
{ 
comment: “comment goes here”, 
parent: { type: “comment or post”, id: parent_id }, 
author: username, 
comments_count: 2, 
updated_at: date 
} 
