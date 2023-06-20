Student Information System
This is a RESTful API that allows you to perform CRUD operations (Create, Read, Update, Delete) on a student database. It is built using Node.js, Express.js, MongoDB, and Mongoose.

Prerequisites
Before running the project, make sure you have the following tools installed:

Node.js
MongoDB
Getting Started
To set up the project, follow these steps:

Clone the repository or download the source code.
Open a terminal and navigate to the project directory.
Install the dependencies by running the following command:

npm install
Configuration
Make sure you have MongoDB installed and running on your local machine. If you have MongoDB installed at a different location or using MongoDB Atlas, modify the connection string in the mongoose.connect method in app.js file accordingly.

Running the Application
To run the application, use the following command:

sql

npm start
The server will start running on port 3000.

API Endpoints
The following endpoints are available in the API:

GET /students: Fetch all students.
GET /students/:id: Fetch a single student by ID.
POST /students: Add a new student.
PUT /students/:id: Update a student by ID.
DELETE /students/:id: Delete a student by ID.
Examples
Fetch all students
bash

GET /students
Response:

json

[
  {
    "_id": "60c3aa3f4b7153186020b72a",
    "name": "John Doe",
    "age": 20,
    "major": "Computer Science",
    "createdDate": "2021-06-11T10:30:15.305Z",
    "updatedDate": "2021-06-12T15:45:20.102Z"
  },
  {
    "_id": "60c3aa3f4b7153186020b72b",
    "name": "Jane Smith",
    "age": 22,
    "major": "Mathematics",
    "createdDate": "2021-06-13T09:15:40.207Z",
    "updatedDate": "2021-06-15T12:20:10.512Z"
  }
]
Fetch a single student
bash

GET /students/60c3aa3f4b7153186020b72a
Response:

json

{
  "_id": "60c3aa3f4b7153186020b72a",
  "name": "John Doe",
  "age": 20,
  "major": "Computer Science",
  "createdDate": "2021-06-11T10:30:15.305Z",
  "updatedDate": "2021-06-12T15:45:20.102Z"
}
Add a new student
bash

POST /students
Request body:

json

{
  "name": "Alice Johnson",
  "age": 19,
  "major": "Physics"
}
Response:

json

{
  "_id": "60c3aa3f4b7153186020b72c",
  "name": "Alice Johnson",
  "age": 19,
  "major": "Physics",
  "createdDate": "2021-06-17T08:55:30.409Z",
  "updatedDate": "2021-06-17T08:55:30.409Z"
}
Update a student
bash

PUT /students/60c3aa3f4b7153186020b72a
Request body:

json

{
  "age": 21
}
Response:

json

{
  "_id": "60c3aa3f4b7153186020b72a",
  "name": "John Doe",
  "age": 21,
  "major": "Computer Science",
  "createdDate": "2021-06-11T10:30:15.305Z",
  "updatedDate": "2021-06-18T14:10:45.718Z"
}

Delete a student
bash

DELETE /students/60c3aa3f4b7153186020b72c
Response:

json

{
  "message": "Student deleted successfully"
}
Error Handling
If an error occurs during any operation, the API will return an appropriate HTTP status code along with an error message in the response body.

Conclusion
You have successfully set up and run the Student Information System API. You can use tools like Postman to test the API endpoints and perform CRUD operations on the student database.
