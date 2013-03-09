##User
(CRUD)  
###get all users  
```
GET /users
```
###get all courses  
```
GET /users/:user/courses
```
###get all problem sets in course  
```
GET /users/:user/:course/sets
```
###get/update a problem set in a course   
```
GET /users/:user/:course/:set
```
```
POST /users/:user/:course/:set
```
###add(assign)/remove problem set  
```
POST /users/:user/:course/:set
```
```
DELETE /users/:user/:course/:set
```
###get grade for a set  
```
GET /users/:user/:course/:set/grade
```