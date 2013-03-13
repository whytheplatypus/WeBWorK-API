##User
(CRUD)  
###get all users  
```
GET /users

return [ User ]

permissions: > Student
```
###get all courses  
```
GET /users/:user/courses

return [ Course ]

permissions: > Student  || if user==:user then Student
```
###get all problem sets in course  
```
GET /users/:user/:course/sets

return [ProblemSet] or [UserSet]

permissions: > Student  || if user==:user then Student
```
###get/update a problem set in a course   
```
GET /users/:user/:course/:set

return a single ProblemSet or UserSet

permissions: > Student  || if user==:user then Student

```
```
POST /users/:user/:course/:set

return  the set

permissions: > Student

```
###add(assign)/remove problem set  
```
PUT /users/:user/:course/:set

return  the set

permissions: > Student
```
```
DELETE /users/:user/:course/:set

return  the set

permissions: > Student

```
###get grade for a set  
```
GET /users/:user/:course/:set/grade

return a Grade (or a number)

permissions: > Student  || if user==:user then Student

```
