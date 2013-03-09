## Problem Set  
(CRUD)  
###get all users  
```
GET /courses/:course/problemset/:problemset/users
```
###get/update *problem* for a *user*  
```
GET /courses/:course/problemset/:problemset/users/:user/:problem
```
```
PATCH /courses/:course/problemset/:problemset/users/:user/:problem
```
###add/remove *problem*  
```
POST /courses/:course/problemset/:problemset/:problem
```
```
DELETE /courses/:course/problemset/:problemset/:problem
```
###add/remove *users*  
```
POST /courses/:course/problemset/:problemset/:problem
```
```
DELETE /courses/:course/problemset/:problemset/:problem
```
###get grade for a *user*  
```
GET /courses/:course/problemset/:problemset/user/:user/grade
```
###get past answers for a *user*  
```
GET /courses/:course/problemset/:problemset/user/:user/pastanswers
```
###regrade a *problem*
```
GET /courses/:course/problemset/:problemset/regrade/:problem
```
