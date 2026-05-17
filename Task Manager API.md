# Task Manager API Documentation
This is a documentation for a sample **Task Manager API**. 

## 1 Overview
The Task Manager API allows developers to interact with user to-do lists. It supports to retrieve complete list of tasks or to see individual tasks by their unique identifier.
* **Base URL:** `https://jsonplaceholder.typicode.com`
* **Format:** JSON
* **Authentication:** None (Public API)

## 2 Endpoints
### 1. Get All Tasks
Retrieves a list of all to-do tasks available in the system.
* **HTTP Method:** `GET`
* **Path:** `/todos`
* **Query Parameters:**
  | Parameter | Type | Required | Description |
  | :--- | :--- | :--- | :--- |
  | `completed` | boolean | No | Filters tasks by their completion status (`true` or `false`). |

  #### Code Example (cURL)
```bash```

curl --location '[https://jsonplaceholder.typicode.com/todos](https://jsonplaceholder.typicode.com/todos)'

#### Sample Response (200 OK)
```JSON```

`[
  {
    "userId": 1,
    "id": 1,
    "title": "delectus aut autem",
    "completed": false
  }
]`
### 2. Get Task by ID
Retrieves the details of a single specific task.
* **HTTP Method:** `GET`
* **Path:** `/todos/{id}`
* Path Parameters:
  | Parameter | Type | Required | Description |
  |-----------|------|----------|-------------|
  |`id`| integer | Yes | The unique identifier of the task.|
  
   #### Code Example (cURL)
```bash```

curl --location '[https://jsonplaceholder.typicode.com/todos/1](https://jsonplaceholder.typicode.com/todos/1)'

#### Sample Response (200 OK)

```JSON```

`{
  "userId": 1,
  "id": 1,
  "title": "delectus aut autem",
  "completed": false
}`

#### Sample Response (404 Not Found)
Returned if the requested task ID does not exist.
```JSON```
`{}`
