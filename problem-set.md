## Problem Set  
(CRUD)  
###get all sets  
Get all sets for course *course_id* 
```
GET /courses/:course_id/sets

return [ProblemSet]

Permissions:  > student
```

###Get/Add/Update/Delete a particular set for a particular course

These are GlobalSet actions. 

Get set *set_id* for course *course_id*
```
GET /courses/:course_id/sets/:set_id

return ProblemSet

Permission: > Student || Student if user == user_id
```

Add set *set_id* to course *course_id*
```
POST /courses/:course_id/sets/:set_id

return ProblemSet

Permission:  > Student

```
Update set *set_id* to course *course_id*
```
PUT/PATCH /courses/:course_id/sets/:set_id

return ProblemSet

Permission:  > Student
```

Delete set *set_id* to course *course_id*

```
DELETE /courses/:course_id/sets/:set_id

return ProblemSet

Permission:  > Student
```

### Get/Add/Update/Delete a particular set for a user in a course

These are UserSet actions. 

Get the ProblemSet properties for set *set_id* for user *user_id* in course *course_id* 

```
GET /courses/:course_id/sets/:set_id/users/:user_id

return UserSet

Permission:  > Student || Student if user==user_id

```

Add the ProblemSet properties for set *set_id* for user *user_id* in course *course_id* 

```
POST /courses/:course_id/sets/:set_id/users/:user_id

return UserSet

Permission:  > Student 

```

Update the ProblemSet properties for set *set_id* for user *user_id* in course *course_id* 

```
PUT/PATCH /courses/:course_id/sets/:set_id/users/:user_id

return UserSet

Permission:  > Student 

```

Delete the ProblemSet properties for set *set_id* for user *user_id* in course *course_id* 

```
DELETE /courses/:course_id/sets/:set_id/users/:user_id

return UserSet

Permission:  > Student 

```
### Get/Assign/Update/unassign a set of users from a set in a course

Get the assigned users for set *set_id* in course *course_id*

```
GET /course/:course_id/sets/:set_id/users

return [user_id]

Permission: > Student
```

Assign users *assigned_users* for set *set_id* in course *course_id*

```
POST /course/:course_id/sets/:set_id/users

return [user_id]

Permission: > Student
```

Updated the properties of set *set_id* for  users *assigned_users* in course *course_id*

```
PUT /course/:course_id/sets/:set_id/users

return UserPropertyHash

Permission: > Student
```

Unassign users *assigned_users* for set *set_id* in course *course_id*

```
DELETE /course/:course_id/sets/:set_id/users

return [user_id]

Permission: > Student
```


