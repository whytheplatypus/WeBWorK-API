## Problem Set  
(CRUD)  
###get all users  
Get all users for course *course_id* and set *set_id*
```
GET /courses/:course_id/:set_id/users

Returns [user_id]

Permissions:  > student
```
###get/update a problem for a user in a problem set

Get problem *problem_id* for user *user_id* with set *set_id* and course *course_id*
```
GET /courses/:course_id/:set_id/users/:user_id/:problem_id
```
```
PUT/PATCH /courses/:course_id/:set_id/users/:user_id/:problem_id
```
###add/remove *problem*  
```
POST /courses/:course/:problemset/:problem
```
```
DELETE /courses/:course/:problemset/:problem
```
###add/remove *users*  
```
POST /courses/:course/:problemset/:problem
```
```
DELETE /courses/:course/:problemset/:problem
```
###get grade for a *user*  
```
GET /courses/:course/:problemset/user/:user/grade
```
###get past answers for a *user*  
```
GET /courses/:course/:problemset/user/:user/pastanswers
```
###regrade a *problem*
```
GET /courses/:course/:problemset/regrade/:problem
```
