# Quizzer API

## Getting Started
Install dependencies:

```bash
npm install
```

Start the server:

```bash
node index.js
```

## Endpoints

### Quizzes

**`GET` /quizzes**  
Returns a list of all quizzes

**`GET` /quizzes/:id**  
Returns a single quiz

### Questions

**`PUT` /quizzes/:id/questions/:questionId**  
Updates an entire question

**`POST` /quizzes/:id/questions/:questionId**  
Returns the specified quiz with added question

**`DELETE` /quizzes/:id/questions/:questionId**  
Removes the specified question

### Answers

**`PUT` /quizzes/:id/questions/:questionId/:answerId**  
Updates an entire answer within a question.

**`POST` /quizzes/:id/questions/:questionId/:answerId**  
Returns the specified question with the added answer

**`DELETE` /quizzes/:id/questions/:questionId/:answerId**  
Removes the specified answered

### Scores

**`POST` /scores/:scoreValue**  
Returns a detailed score summary


