### API-sidetips

- dataportal.se
- kolada.se

---

# Welcome to Python!

- Popular programming language for web development and automation.
- Why Python? Readable, versatile, and widely supported by a large community.

---

## Python vs. C++: An Overview

- **Python**: Interpreted, high-level, dynamically typed.
- **C++**: Compiled, can be low-level, statically typed.

---

### Example: Hello World

- Python:

```python
print("Hello, World!")
```

- C++:

```cpp
#include <iostream>
using namespace std;
int main() {
    cout << "Hello, World!";
    return 0;
}
```

---

### Python Syntax Basics

- Simple and easy to learn syntax.
- Focus on readability and efficiency.

---

#### Example: For Loop

- Python:

```python
for i in range(5):
    print(i)
    print(i)
```

- C++:

```cpp
for (int i = 0; i < 5; i++) {
    cout << i << endl;
}
```

---

https://diveintopython3.net/

---

### Prova

```bash
python --version
python3 --version
```

```
>>>
```

---

### Why Use Virtual Environments?

- Isolates Python projects to avoid dependency conflicts.
- Each project can have its own dependencies, irrespective of what dependencies every other project has.

### Creating a Virtual Environment

```bash
python -m venv myprojectenv
source myprojectenv/bin/activate  # On Windows use `myprojectenv\Scripts\activate`
```

---

### Introduction to Poetry for Dependency Management

- Handles project dependencies and packaging in a simple and intuitive way.
- Automatically manages a virtual environment for your projects.

---

### Initializing a Project with Poetry

```bash
poetry init
poetry add requests
```

---

### Basic Commands in Poetry

- Start a new project: `poetry new myproject`
- Install dependencies: `poetry install`
- Add a new dependency: `poetry add packagename`

---

```bash
poetry new kulprojekt
cd kulprojekt
poetry install
poetry add fastapi
```

---

### Example: Adding a Dependency

```bash
poetry add numpy
```

---

### Summary

- Python offers a clear syntax and powerful frameworks and libraries for web development.
- Virtual environments and tools like Poetry make dependency management simpler and more effective.

---

# Bygga REST API:er

Note:
In this part, we'll discuss the basics of REST, which stands for Representational State Transfer. REST is an architectural style for designing networked applications. It relies on a stateless, client-server, cacheable communications protocol -- the HTTP. RESTful applications use HTTP requests to post data (create and/or update), read data (e.g., make queries), and delete data. Thus, REST uses HTTP for all four CRUD (Create/Read/Update/Delete) operations.

---

## Vad är ett REST API?

- CRUD-operationer: Create, Read, Update, Delete.
- HTTP-metoder: GET, POST, PUT, DELETE.

Note:
When designing APIs, it's crucial to make them intuitive and easy to use. This involves using standard HTTP methods clearly and consistently. For instance, GET requests should only fetch data and not change any state on the server. POST is used to create new resources, and PUT is for updating existing resources. DELETE, as the name suggests, is used to remove resources. Keeping to these standards makes your API predictable and easier to integrate with.

---

### PUT vs POST

- **PUT**: Idempotent, används för att uppdatera resurser. Kan användas flera gånger utan att ändra resultatet.
- **POST**: Non-idempotent, används för att skapa nya resurser. Kan ge olika resultat vid flera anrop.

---

### Statuskoder i HTTP

Note:
HTTP status codes are critical in REST APIs as they inform the client about the result of their request. Common codes include 200 for a successful GET, POST, or PUT request, 201 for a resource successfully created using POST, 404 for resource not found, and 500 for an internal server error. These codes help the client to understand whether their request was successful, or if something went wrong, and how to proceed.

---

### Börja med FastAPI

Note:
Now, let's set up our environment for developing with FastAPI. We'll use Poetry to manage our dependencies. First, we install FastAPI and Uvicorn, which is an ASGI server that will serve our API. You can install these using Poetry by running `poetry add fastapi uvicorn`. This command adds FastAPI and Uvicorn to your project's dependencies and installs them.

---

### main.py

```python
from fastapi import FastAPI

app = FastAPI()
```

Note:
Let's start by creating a basic FastAPI application. Create a new Python file, for example, `main.py`, and import FastAPI from the fastapi module. Then, create an instance of FastAPI by declaring `app = FastAPI()`. This instance is now ready to be used to define endpoints.

---

```python
@app.get("/")
def read_root():
    return {"Hello": "World"}
```

Note:
Implement your first endpoint using the GET method. Define a function that will respond to HTTP GET requests. You can do this by decorating a function with `@app.get("/")`. Inside the function, simply return a message like `{"Hello": "World"}`. This endpoint will now return a JSON response containing a greeting message whenever the root URL is accessed via a GET request.

---

### Lägg till POST, PUT, DELETE

Note:
Next, let's add more functionality to our API by implementing endpoints for POST, PUT, and DELETE. These endpoints will allow users to create, update, and delete data respectively. Each endpoint uses a similar decorator but with different HTTP methods and potentially different paths and function parameters.

---

### Parametrar

- Path
- Query

Note:
FastAPI makes it easy to work with both path parameters and query parameters. Path parameters are part of the URL path, for example in `/items/{item_id}`, where `item_id` is a variable part of the URL. Query parameters are appended at the end of the URL after a question mark, like `/items?name=widget`. Both types of parameters can be dynamically captured and used in your endpoint functions.
