##Courses
(CRUD)  
###get all *users*  
```
GET /courses/:course_id/users

return [User]

permissions: > Student
```
###get all problems sets for course *course_id*
```
GET /courses/:course_id/sets

return [ProblemSet]

permissions: > Student
```
###add/remove *user_id* from course *course_id*  
```
POST /courses/:course_id/users/:user_id

return User

permission: > Student
```
```
DELETE /course/:course_id/users/:user_id

return User

permission: > Student
```

###update *user_id* in course *course_id*
```
PUT/PATCH /courses/:course_id/users/:user_id

return User

permission: > Student
```
