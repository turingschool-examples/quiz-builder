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

##### `GET` /quizzes  
Returns a list of all quizzes

##### `GET` /quizzes/:quizId  
Returns a single quiz

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID

-----------------------------------------------

### Questions

##### `POST` /quizzes/:quizId/questions  
Returns the specified quiz with added question

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID


* **Body Content:**  
  * You must pass in a full question object like so:

```json
{
  "title": "Question Title",
  "answers": []
}
```

##### `PUT` /quizzes/:quizId/questions/:questionId  
Updates an entire question

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID
  * **questionId:** *(required)* <String> - the question ID


* **Body Content:**  
  * You must pass in a full question object like so:

```json
{
  "title": "Question Title",
  "answers": []
}
```

##### `DELETE` /quizzes/:quizId/questions/:questionId  
Removes the specified question

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID
  * **questionId:** *(required)* <String> - the question ID

-----------------------------------------------

### Answers

##### `POST` /quizzes/:quizId/questions/:questionId/answers  
Returns the specified question with the added answer

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID
  * **questionId:** *(required)* <String> - the question ID


* **Body Content:**  
  * You must pass in a full answer object like so:

```json
{
  "title": "Answer title",
  "score": 5
}
```

##### `PUT` /quizzes/:quizId/questions/:questionId/answers/:answerId  
Updates an entire answer within a question.

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID
  * **questionId:** *(required)* <String> - the question ID
  * **answerId:** *(required)* <String> - the answer ID


* **Body Content:**  
  * You must pass in a full answer object like so:

```json
{
  "title": "Answer title",
  "score": 5
}
```

##### `DELETE` /quizzes/:quizId/questions/:questionId/:answerId  
Removes the specified answered

* **Parameters:**  
  * **quizId:** *(required)* <String> - the quiz ID
  * **questionId:** *(required)* <String> - the question ID
  * **answerId:** *(required)* <String> - the answer ID

-----------------------------------------------

### Scores

##### `POST` /scores/:scoreValue  
Submits a user's score and returns a detailed score summary

* **Parameters:**  
  * **scoreValue:** *(required)* <Integer> - a numeric score


