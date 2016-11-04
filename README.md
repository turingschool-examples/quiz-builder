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

**`POST` /quizzes/:id/questions/:questionId**
Returns the specified quiz with added question