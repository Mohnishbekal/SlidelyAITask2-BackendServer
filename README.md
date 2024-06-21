# SlidelyAITask2-BackendServer
Backend server using Typescript and Node.js

# Sllidely Task

This project is a Node.js server application for handling form submissions and providing CRUD operations via HTTP endpoints.

## Features

- **Submit**: Submit a new form with fields `name`, `email`, `phone`, `github_link`, and `stopwatch_time`.
- **Read**: Read a specific form submission by index.
- **Ping**: Always returns `true` to indicate server availability.

## Prerequisites

Ensure you have the following installed on your machine:

- Node.js and npm (Node Package Manager)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your_username/sllidely-task.git
   cd sllidely-task

2.**Install Dependencies:**

npm install

Certainly! Here's a plain text version that you can directly copy and paste into your README.md file on GitHub:

markdown
Copy code
# Sllidely Task

This project is a Node.js server application for handling form submissions and providing CRUD operations via HTTP endpoints.

## Features

- **Submit**: Submit a new form with fields `name`, `email`, `phone`, `github_link`, and `stopwatch_time`.
- **Read**: Read a specific form submission by index.
- **Ping**: Always returns `true` to indicate server availability.

## Prerequisites

Ensure you have the following installed on your machine:

- Node.js and npm (Node Package Manager)

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your_username/sllidely-task.git
   cd sllidely-task
Usage
Start the server:
npm start

The server runs at http://localhost:3000.

Ping Endpoint
URL: /ping
Method: GET
Description: Always returns true to indicate server availability.

Submit Endpoint
URL: /submit
Method: POST
Request Payload: JSON with fields:
name: Name of the submitter.
email: Email address of the submitter.
phone: Phone number of the submitter.
github_link: GitHub link of the submitter.
stopwatch_time: Time recorded by the stopwatch.

Example:

curl -X POST http://localhost:3000/submit -H "Content-Type: application/json" -d '{
  "name": "John Doe",
  "email": "john.doe@example.com",
  "phone": "123-456-7890",
  "github_link": "https://github.com/johndoe",
  "stopwatch_time": "00:01:30"
}'


Read Endpoint
URL: /read
Method: GET
Query Parameter: index (0-indexed position of the submission)
Response: JSON object representing the submission details.

curl http://localhost:3000/read?index=0
