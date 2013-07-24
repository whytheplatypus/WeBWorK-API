##Problem Render
###get rendered (id, path, code)  
```
GET /problem

returns [RenderedProblem]

permisssion: > Student || if Student only assigned problem to be returned. 
```
body contains id, path, code
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
