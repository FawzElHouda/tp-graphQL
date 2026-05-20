
# Task Management API with GraphQL

A powerful Task Management API built with GraphQL, Node.js, Express, and Apollo Server. This API provides complete CRUD operations for managing tasks with a flexible GraphQL interface.

## ✨ Features

- 🔍 Query all tasks or a single task by ID
- ➕ Add new tasks with title, description, status, and duration
- ✅ Mark tasks as completed
- 📝 Change task descriptions
- 🗑️ Delete tasks
- 🎯 Task properties: ID, title, description, completed status, duration
- 🚀 Apollo Sandbox for interactive API testing

## 🛠️ Tech Stack

- **Node.js** - JavaScript runtime
- **Express** - Web framework
- **Apollo Server** - GraphQL server
- **GraphQL** - Query language for APIs

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- Git

## 🚀 Local Installation

1. **Clone the repository**
```bash
git clone https://github.com/FawzElHouda/tp-graphql.git
cd tp-graphql

2. Install dependencies:
npm install

3.Start the server
node index.js


4.Open Apollo Sandbox
http://localhost:5000/graphql


📖 GraphQL API Documentation
Queries
Get all tasks:
query {
  tasks {
    id
    title
    description
    completed
    duration
  }
}

Get a single task by ID:
query {
  task(id: "1") {
    id
    title
    description
    completed
    duration
  }
}


Mutations
Add a new task:
mutation {
  addTask(
    title: "Learn GraphQL"
    description: "Complete the GraphQL tutorial"
    completed: false
    duration: 5
  ) {
    id
    title
    description
    completed
    duration
  }
}

Mark a task as completed:
mutation {
  completeTask(id: "1") {
    id
    title
    completed
  }
}

Change task description:
mutation {
  changeDescription(
    id: "1"
    newDescription: "Updated task description"
  ) {
    id
    title
    description
  }
}

Delete a task:
mutation {
  deleteTask(id: "2") {
    id
    title
  }
}


🧪 Testing with Postman
1.Create a new request

Method: POST
URL: http://localhost:5000/graphql

2.Set Headers:
Content-Type: application/json

3.Body (raw JSON):
{
  "query": "query { tasks { id title description completed duration } }"
}

