# Task API

A simple CRUD To-Do API built using Python and FastAPI.

## Features

* Create tasks
* Read tasks
* Update tasks
* Delete tasks
* Input validation
* In-memory data storage
* Swagger UI documentation

## Technologies

* Python 3.10+
* FastAPI
* Uvicorn

## Installation

Clone the repository:

```bash
git clone https://github.com/yasha-tech/task-api.git
cd task-api
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the virtual environment on Windows:

```bash
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Running the API

Start the server with:

```bash
uvicorn main:app --reload
```

The API will run at:

```text
http://127.0.0.1:8000
```

Swagger UI is available at:

```text
http://127.0.0.1:8000/docs
```

## API Endpoints

| Method | Endpoint      | Description       |
| ------ | ------------- | ----------------- |
| GET    | `/`           | API information   |
| GET    | `/health`     | Health check      |
| GET    | `/tasks`      | Get all tasks     |
| GET    | `/tasks/{id}` | Get a single task |
| POST   | `/tasks`      | Create a new task |
| PUT    | `/tasks/{id}` | Update a task     |
| DELETE | `/tasks/{id}` | Delete a task     |

## curl -i Example

Command:

```bash
curl -i http://127.0.0.1:8000/tasks/1
```

Output:

```text
date: Fri, 31 Jul 2026 12:10:52 GMT
server: uvicorn
content-length: 45
content-type: application/json

{"id":1,"title":"Learn FastAPI","done":false}
```

## Swagger UI

![Swagger UI](swagger.png)
