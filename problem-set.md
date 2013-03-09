## Problem Set  
(CRUD)  
###get all users  
```
GET /courses/:course/:problemset/users
```
###get/update *problem* for a *user*  
```
GET /courses/:course/:problemset/users/:user/:problem
```
```
PATCH /courses/:course/:problemset/users/:user/:problem
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
