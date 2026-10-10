Internship REST API — EdVyro Task 2

A beginner-friendly REST API for managing internship records, built with Node.js, Express.js, and SQLite. The API supports CRUD operations, pagination, input validation, and persistent data storage.

📌 Project Overview

The Internship REST API provides endpoints to create, retrieve, update, and delete internship records. It uses SQLite for persistent storage and Express.js to handle HTTP requests and responses.

This project was developed as part of the EdVyro Full Stack Development Internship — Task 2.

🚀 Technologies Used
Node.js — JavaScript runtime environment
Express.js — Backend web framework
SQLite — Lightweight relational database
better-sqlite3 — SQLite database integration for Node.js
npm — Package management
✨ Features
RESTful API architecture
Complete CRUD operations for internship records
SQLite database persistence
Pagination support for listing internships
Input validation and error handling
Appropriate HTTP status codes
Health-check endpoint
Easy local setup and execution
📂 Project Structure
internship-rest-api/
├── package.json
├── package-lock.json
├── server.js
├── seed.js
├── database.js
├── internships.db
└── README.md


Note: The exact filenames may vary depending on your implementation. Do not include generated database files or other files unless they are part of your project.

⚙️ Prerequisites

Before running the project, ensure you have installed:

Node.js
npm (included with Node.js)
Git (for version control and GitHub submission)
🛠️ Installation and Setup

1. Clone the repository

git clone <YOUR_GITHUB_REPOSITORY_URL>


2. Navigate to the project directory

cd internship-rest-api


3. Install dependencies

npm install


4. Seed the database

npm run seed


5. Start the server

npm start


The API will be available at:

http://localhost:3000

🔍 Health Check

Use the health-check endpoint to verify that the server is running.

Endpoint: GET /health

curl http://localhost:3000/health

📡 API Endpoints

Base URL: http://localhost:3000

HTTP Method	Endpoint	Description
GET	/internships?page=1&limit=5	Retrieve internships with pagination
GET	/internships/:id	Retrieve a specific internship
POST	/internships	Create a new internship
PUT	/internships/:id	Update an existing internship
DELETE	/internships/:id	Delete an internship
GET	/health	Check server health
📝 API Usage Examples
1. Get All Internships

Retrieve internship records with pagination.

curl "http://localhost:3000/internships?page=1&limit=5"

2. Get an Internship by ID
curl http://localhost:3000/internships/1

3. Create a New Internship

Send a POST request with a JSON request body.

curl -X POST http://localhost:3000/internships \
  -H "Content-Type: application/json" \
  -d '{
    "title": "React Intern",
    "company": "WebWorks",
    "domain": "Web Development",
    "location": "Remote",
    "duration": "8 weeks",
    "level": "Beginner",
    "description": "Build accessible web interfaces."
  }'

4. Update an Internship

Send a PUT request with the internship ID and updated information.

curl -X PUT http://localhost:3000/internships/1 \
  -H "Content-Type: application/json" \
  -d '{
    "title": "Frontend Developer Intern",
    "company": "NovaByte Labs",
    "domain": "Web Development",
    "location": "Remote",
    "duration": "10 weeks",
    "level": "Beginner",
    "description": "Build responsive web interfaces."
  }'

5. Delete an Internship
curl -X DELETE http://localhost:3000/internships/1


Note: These examples assume the API accepts the listed fields and uses numeric internship IDs.

📋 Validation and HTTP Status Codes
Status Code	Meaning
200 OK	Request completed successfully
201 Created	Internship created successfully
400 Bad Request	Invalid ID or validation error
404 Not Found	Internship or route not found
500 Internal Server Error	Unexpected server error
💾 Database

The application uses SQLite to store internship records persistently.

The database is initialized by the application's database setup logic, and the seed script populates it with sample internship records.

The included records are fictional demonstration data. If EdVyro provides an official dataset or database schema, use the supplied records and schema for the final submission.

🧪 Testing

You can test the API using:

cURL — Send HTTP requests from the terminal.
Postman — Test endpoints and inspect responses.
Browser — Access the health-check endpoint and GET endpoints.

Verify that listing, retrieval, creation, updating, deletion, pagination, validation, and error handling work as expected.

📤 Submission Instructions
Ensure the project runs locally without errors.
Test all required API endpoints.
Push the complete project folder to a public GitHub repository.
Confirm that the repository contains the source code and README.
Submit the public GitHub repository URL as the single proof link.
👨‍💻 Project Information
Project: Internship REST API
Organization: EdVyro
Program: Full Stack Development Internship
Task: Task 2
Category: Backend Development

Built with Node.js, Express.js, and SQLite.
