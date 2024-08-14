# JudgeBackend

## Protocal

Structure of different types of data.

### User

```json
{
    "_id": String,
    "username": String,
    "displayName": String,
    "password": String,
    "isAdmin": Boolean,
    "solvedProblem": Number,
    "solvedProblems": [String],
    "rating": Number,
}
```

### Problem

```json
{
    "_id": String,
    "displayID": String,
    "title": String,
    "description": String,
    "inputFormat": String,
    "outputFormat": String,
    "timeLimit": Number,
    "memoryLimit": Number,
    "scorePolicy": String,
    "testcases": [
        {
            "input": String,
            "output": String,
            "point": Number,
            "subtask": String
        }
    ]
}
```

### Submission

```json
{
    "_id": String,
    "when": String,
    "status": String,
    "language": String,
    "username": String,
    "problemId": String,
    "result": {
        "type": String,
        "maxTime": Number,
        "maxMemory": Number,
        "individual": [
            {
                "type": String,
                "time": Number,
                "memory": Number
            }
        ]
    },
    
}
```

## API

- User
    - GET /api/users
    - POST /api/users
- Problems
    - GET /api/problems
    - POST /api/problems