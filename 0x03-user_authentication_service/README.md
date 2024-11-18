# 0x03. User Authentication Service

## **Project Overview**
This project is about implementing a **User Authentication Service** using Flask. Although real-world applications often use established frameworks or modules (e.g., Flask-User) for authentication, this project will guide you through the step-by-step process of building a basic authentication mechanism to deepen your understanding of how these systems work.

---

## **Learning Objectives**
By the end of this project, you should be able to:
1. **Declare API Routes**:
   - Understand how to define endpoints in a Flask app to handle different HTTP requests (e.g., `GET`, `POST`).

2. **Handle Cookies**:
   - Learn how to set and retrieve cookies in HTTP responses and requests.

3. **Retrieve Request Data**:
   - Access data sent through request forms and process it effectively.

4. **HTTP Status Codes**:
   - Return appropriate HTTP status codes to indicate the success or failure of an operation.

---

## **Requirements**
- **Python Version**: All files must be compatible with Python 3.7.
- **Flask**: Use Flask to build your backend.
- **SQLAlchemy**: Use SQLAlchemy version `1.3.x` for interacting with the database.
- **Bcrypt**: Install and use `bcrypt` for securely hashing and verifying passwords:
  ```bash
  pip3 install bcrypt
  ```
- **Coding Standards**:
  - Follow `pycodestyle` (version 2.5).
  - Ensure all files are executable and end with a newline.
  - Include documentation for modules, classes, and functions with detailed descriptions.
  - Use type annotations for all functions.

---

## **Key Concepts**
- **Authentication**:
  - Implement a simple system to authenticate users with email and password.
  
- **Database Operations**:
  - Use SQLAlchemy to interact with a database for storing and retrieving user data.

- **Password Security**:
  - Hash passwords using `bcrypt` to ensure they are securely stored.

- **Session Management**:
  - Manage user sessions using cookies to maintain a user's login state.

---

## **Setup**
1. Install **Flask** and **Bcrypt**:
   ```bash
   pip3 install flask bcrypt
   ```

2. Create a database using SQLAlchemy for managing user information.

3. Define an `Auth` class to encapsulate authentication-related methods:
   - `register_user(email, password)`
   - `login_user(email, password)`
   - `logout_user()`
   - `get_user_from_session_token(token)`

4. Ensure your Flask app only interacts with the **Auth** class and not directly with the database.

---

## **Example**

### **Registering a User**
```bash
POST /register
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

### **Login**
```bash
POST /login
{
  "email": "user@example.com",
  "password": "securepassword"
}
```

### **Response**
```json
{
  "message": "Login successful",
  "session_token": "abc123xyz"
}
```
