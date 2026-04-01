# Task Management API Assignment

## 📌 Overview
This project is a Task Management API built using Node.js and Express.  
The assignment focuses on understanding existing code, identifying bugs, fixing issues, and implementing a new feature.

---

## 🚀 Setup Instructions

1. Clone the repository:
git clone https://github.com/lokeshrathore1509/task-api-assignment.git

2. Navigate to project:
cd task-api

3. Install dependencies:
npm install

4. Start server:
npm start

Server runs on:
http://localhost:3000

---

## 📌 API Endpoints

- GET /tasks → Get all tasks
- POST /tasks → Create task
- PUT /tasks/:id → Update task
- DELETE /tasks/:id → Delete task
- PATCH /tasks/:id/complete → Mark complete
- PATCH /tasks/:id/assign → Assign task

---

## 🐞 Bugs Identified

1. Pagination Bug  
Offset was calculated using `page * limit` instead of `(page - 1) * limit`.

2. Status Filter Bug  
Used `.includes()` which caused incorrect filtering.

3. Priority Reset Bug  
Priority was reset to "medium" when marking task complete.

4. Status Naming Issue  
Different status values like "todo", "done", "in_progress".

5. Missing Validation  
Update API allows invalid fields.

---

## ✅ Bug Fix Implemented

Fixed Pagination Logic:
(page - 1) * limit

---

## ✨ Feature Implemented

### Assign Task API

- Endpoint: PATCH /tasks/:id/assign

#### Request:
{
  "userId": "user123"
}

#### Behavior:
- Adds userId to task
- Returns 404 if task not found
- Returns 400 if userId missing

---

## 🧪 Testing

Tested using Hoppscotch:
- Create task
- Get tasks
- Update task
- Delete task
- Assign task

---

## 📌 Notes

- Data is stored in-memory
- Data resets on server restart

---

## 👨‍💻 Author

Lokesh Rathore
