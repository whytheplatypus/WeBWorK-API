##Problem Render
###get rendered (id, path, code)  
```
GET /problem

returns [RenderedProblem]

permisssion: > Student || if Student only assigned problem to be returned. 
```
body contains id, path, code, user_id, course_id, set_id, ...

* A professor can get a rendered problem for any pgfile (from library or local) for any problem seed
* A student can only get a rendered problem for the given course, set and seed for that student

###check answer (id, path, code)  
```
POST /problem/check

return [boolean]

permission > Student || if Student only assign problem to be checked. 
```
body contains id, path, code and answer

answer is an array of booleans (correct in the order of problems)

###create (code?)  
```
POST /problem/:problem_id

return Problem

permission > Student 

```
body contains code (maybe path?)
