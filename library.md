##Library
###get problems by subject/subsubject/...
```
GET /library/subject

return [libraryTree];

permissions: > Student

```
returns a tree containing all problem categories (subject/chapter/subchapter)

###get problems by directory

```
GET /library/directories

return [libraryTree];

permissions: >Student
```
returns a library Tree by directory/subdirectories.

###search  
```
GET /library/search

return [Problem];

permission: > Student

```
body contains parameters (subject, keyword, ....)

returns an array of problems (or problem_id's) that match the sent criteria.

###get local problems
```
GET /library/:course_id

return [libraryTree]  or [Problems];

permission: > Student
```
returns a tree or a array of problems of all local problems for the course :course_id
