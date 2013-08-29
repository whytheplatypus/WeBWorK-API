##User
(CRUD)  
###get all users  

get all users (from all courses)
```
GET /users

return [ User ]

permissions: > Student
```
###get one user  

get user *user_id*
```
GET /users/:user_id

return User

permissions: > Student || if user==:user then Student
```


###get all courses  

get all courses for user *user_id*
```
GET /users/:user_id/courses

return [ Course ]

permissions: > Student  || if user==:user then Student
```
###get all problem sets in course  

Get all problem sets for user *user_id* and course *course_id*
```
GET /users/:user_id/courses/:course_id/sets

return [ProblemSet] or [UserSet]

permissions: > Student  || if user==:user then Student
```
###get/update a problem set in a course   

Get/update the problem set *set_id* for user *user_id* for course *course_id*

```
GET /users/:user_id/courses/:course_id/sets/:set_id

return a single ProblemSet or UserSet

permissions: > Student  || if user==:user then Student

```
```
POST/PATCH /users/:user_id/courses/:course_id/sets/:set_id

return  the set

permissions: > Student

```
###add(assign)/remove problem set  

Add/assign or remove/delete the problem set *set_id* for user *user_id* and course *course_id*

```
PUT /users/:user_id/courses/:course_id/sets/:set_id

return  the set

permissions: > Student
```
```
DELETE /users/:user_id/courses/:course_id/sets/:set_id

return  the set

permissions: > Student

```
###get grade for a set 

Get the grade for problem set *set_id* for user *user_id* for course *course_id*
```
GET /users/:user_id/courses/:course_id/sets/:set_id/grade

return a Grade (or a number)

permissions: > Student  || if user==:user then Student

```

###get a grade for a particular problem

Get the grade for problem *problem_id* in set *set_id* for user *user_id* for course *course_id*

```
GET /users/:user_id/courses/:course_id/sets/:set_id/problems/:problem_id/grade

return a Grade (or a number)

permissions: > Student  || if user==:user then Student

```

