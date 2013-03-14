#User
(CRUD)  
##get all users  
```
GET /users
```
**returns** \[[User](schema.md/#user)\]  
**permissions** > _Student_


##get all courses  
```
GET /users/:user/courses
```
**returns** \[[Course](schema.md/#course)\]  
**permissions** > _Student_  || if user==:user then Student


##get all problem sets in course  
```
GET /users/:user/:course/sets
```
**returns** \[[ProblemSet](schema.md/#problemset)\] or \[[UserSet](schema.md/#userset)\]


##get/update a problem set in a course   
```
GET /users/:user/:course/:set
```
**returns** [ProblemSet](schema.md/#problemset) or [UserSet](schema.md/#userset)  
```
POST /users/:user/:course/:set
```
**returns** Success/Failure


##add(assign)/remove problem set  
```
PUT /users/:user/:course/:set
```
**returns** Success/Failure  
```
DELETE /users/:user/:course/:set
```
**returns** Success/Failure  


##get grade for a set  
```
GET /users/:user/:course/:set/grade
```
**returns** a Grade (or a number)
