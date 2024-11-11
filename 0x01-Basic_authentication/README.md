# Basic Authentication API

## Project Overview

This project provides a simple RESTful API with user management and implements basic authentication. The purpose is to understand how basic authentication works by implementing it step-by-step.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- **Python 3.7** or above
- **Flask**: Install with `pip install Flask`
- **Other requirements**: Install dependencies with `pip install -r requirements.txt`

### Starting the API

To start the API server:

```bash
API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```

You should now be able to access the API at `http://0.0.0.0:5000/api/v1/status`.

## API Endpoints

### Status Check

- **GET** `/api/v1/status`
- Response: `{"status": "OK"}`

### Unauthorized Access Example

- **GET** `/api/v1/unauthorized`
- Response: `{"error": "Unauthorized"}`, HTTP status `401`

### Forbidden Access Example

- **GET** `/api/v1/forbidden`
- Response: `{"error": "Forbidden"}`, HTTP status `403`

## Error Handling

Custom error handlers are included for unauthorized (401) and forbidden (403) responses.

## Authentication Mechanism

A custom `Auth` class was implemented to handle basic authentication tasks, such as:
- Checking if a route requires authentication (`require_auth`)
- Retrieving the `Authorization` header (`authorization_header`)
- Returning the current user (`current_user`)

The system does not yet implement user credentials validation but lays the foundation for further authentication mechanisms.

## Usage

To test authentication handling, use curl or a tool like Postman:

```bash
curl -H "Authorization: Basic <base64_encoded_credentials>" http://0.0.0.0:5000/api/v1/some_endpoint
```

### Base64 Encoding

To test the API with Basic Auth, you need to encode your username and password in Base64 format, like so:

```python
import base64

credentials = "username:password"
encoded_credentials = base64.b64encode(credentials.encode()).decode()
print(encoded_credentials)  # Use this in the Authorization header
```

---

## Files Structure

- `api/v1/app.py`: Main API application file
- `api/v1/auth/auth.py`: Contains the `Auth` class for handling authentication
- `api/v1/views/index.py`: Contains endpoint definitions
- `requirements.txt`: Lists dependencies for the project
