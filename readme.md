# Simple TODO Java Spring JPA Project

## Endpoints
---
### Create Task
* Method: POST
* URL: `api/tasks`
* Request Body:
```JSON
{
    "title": "string",
    "description": "string (optional)",
    "isCompleted": "Boolean"
}
```

### Get All Tasks
* Method: GET
* URL: `api/tasks`
* Response: `List<Task>`
```JSON
{
    {
        "title": "Task 1",
        "description": "Desc",
        "isCompleted": "false"
    },
    {
        "title": "Task 2",
        "description": "Desc",
        "isCompleted": "true"
    },
    ...
}
```

### Get Task By Id
* Method: GET
* URL: `api/tasks/{id}`
* Path Variable: `id` (Long) GeneratedValue.IDENTITY
* Response: Model.Task Object
```JSON
{
    "id": "Long",
    "title": "String",
    "description": "String",
    "isCompleted": "Boolean"
}
```

### Get Completed Tasks
* Method: GET
* URL: `api/tasks/completed`
* Response: List<Task>
```JSON
{
    {
        "title": "Task 1",
        "description": "Desc",
        "isCompleted": "true"
    },
    {
        "title": "Task 2",
        "description": "Desc",
        "isCompleted": "true"
    },
    ...
}
```

### DELETE Task
* Method: DELETE
* URL: `api/tasks/{id}`
* Path Variable: `id` (Long) GeneratedValue.IDENTITY
* Response: No content / `"ok"` string
```JSON
{
    "ok"
}
```