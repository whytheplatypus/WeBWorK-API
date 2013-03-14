#WeBWorK Request/Response Schemas
This is the Schema for the standard objects WeBWorK deals with.  Any back end will have to implement an [ORM](http://en.wikipedia.org/wiki/Object-relational_mapping) so that it can speak the same language.  In some cases, such as [Mongo](http://www.mongodb.org/), [Couch](http://couchdb.apache.org/), and other JSON stores, there's a good chance that the mapping will come for free.

##User
```javascript
{
  id: String,
  first_name: String,
  last_name: String,
  email: String,
  login_id: String,  // or pehaps its better to just use the email.
  hashed_password: String,
  salt: Number,
}
```
##ProblemSet
references [ProblemPool](#problempool), [UserSetProperty](#usersetproperty), [GlobalSetProperty](#globalsetproperty) 

```javascript
{
  id: String,
  set_name: String,
  problems: [ProblemPool],
  users_properties: [UserSetProperty],
  course_properties: GlobalSetProperty,
}
```
##Course
references [User](#user), [ProblemSet](#problemset)
```javascript
{
  id: String,
  course_name: String,
  users: [User],
  problem_sets: [ProblemSet],
}
```
##SetProperty
```javascript
{
  open_date: Date,
  reduced_credit_date: Date,
  due_date: Date,
  answer_date: Date,
}
```
##GlobalSetProperty  extends SetProperty
```javascript
{

}
```
##UserSetProperty extends SetProperty
```javascript
{
  user: user_id
}
```
##HomeworkSet extends ProblemSet
```javascript
{

}
```
##GatewayQuiz extends ProblemSet
```javascript
{

}
```
##AdaptiveProblemSet extends ProblemSet  // this is a seqence of problems that require the student to go in order.
```javascript
{
  dependencies: [String], // this will be an Array of problem_ids that each problem depends on.  
}
```
##ProblemPool
references [Problem](#problem)
```javascript
{
  id: String,
  pool: [Problem]
}
```
##Problem
```javascript
{
  id: String,
  name: String,
  index: Number, // (or int) 
  weight: Number, // the maximum value
  source: String, // the path or an id if we switch to a database of problems. 
}
```
##Library
references [LibraryProblem](#libraryproblem)
```javascript
{
  name: String,
  problems: [LibraryProblem]
}
```
##LibraryProblem
references [Textbook](#textbook)
```javascript
{
  path: String,
  subject: String,
  chapter: String,
  section: String,
  author: String,
  date_created: Date,
  date_last_modified: Date,
  institution: String,
  text_origin: Textbook
}
```  
