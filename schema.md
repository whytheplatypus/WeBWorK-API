#WeBWorK Schemas
  ##User
  ```
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
  ```
  {
    id: String,
    set_name: String,
    problems: [ProblemPool],
    users_properties: [UserSetProperty],
    course_properties: GlobalSetProperty,
  }
  ```
  ##Course
  ```
  {
    id: String,
    course_name: String,
    users: [User],
    problem_sets: [ProblemSet],
  }
  ```
  ##SetProperty
  ```
  {
    open_date: Date,
    reduced_credit_date: Date,
    due_date: Date,
    answer_date: Date,
  }
  ```
  ##GlobalSetProperty  extends SetProperty
  ```
  {

  }
  ```
  ##UserSetProperty extends SetProperty
  ```
  {
    user: user_id
  }
  ```
  ##HomeworkSet extends ProblemSet
  ```
  {
  
  }
  ```
  ##GatewayQuiz extends ProblemSet
  ```
  {
  
  }
  ```
  ##AdaptiveProblemSet extends ProblemSet  // this is a seqence of problems that require the student to go in order.
  ```
  {
    dependencies: [String], // this will be an Array of problem_ids that each problem depends on.  
  }
  ```
  ##ProblemPool
  ```
  {
    id: String,
    pool: [Problem]
  }
  ```
  ##Problem
  ```
  {
    id: String,
    name: String,
    index: Number, // (or int) 
    weight: Number, // the maximum value
    source: String, // the path or an id if we switch to a database of problems. 
  }
  ```
  ##Library
  ```
  {
    name: String,
    problems: [LibraryProblem]
  }
  ```
  ##LibraryProblem
  ```
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
