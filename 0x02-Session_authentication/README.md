# 0x02. Session Authentication

## Description
In this project, you will build a simple Session Authentication system from scratch to understand how session authentication mechanisms work. Although real-world applications use established libraries or frameworks for session handling, implementing it manually here will provide foundational knowledge in authentication mechanisms, cookies, and session management.

## Learning Objectives
By the end of this project, you will be able to:
- Explain what authentication and session authentication mean.
- Understand and handle HTTP cookies.
- Know how to send and parse cookies for session management.

## Requirements
- **Python Version**: 3.7
- **Platform**: Ubuntu 18.04 LTS
- **Style Guide**: Pycodestyle (version 2.5)
- **Documentation**: Required for all modules, classes, and functions.

## Project Setup
1. Make sure Python 3.7 is installed on your system.
2. Use `#!/usr/bin/env python3` as the first line in all Python scripts.
3. Ensure all files are executable and end with a new line.

## Key Concepts
- **Session Authentication**: A technique to manage user sessions, typically through session IDs stored in cookies.
- **HTTP Cookies**: Used to store session data on the client side, which the server can access to maintain session state.
- **Flask**: A lightweight web framework for handling HTTP requests and responses.

## Usage
After implementing session authentication, you should be able to:
1. Create a session for an authenticated user.
2. Use cookies to manage and persist session data.
3. Parse cookies on incoming requests to authenticate users based on session information.

## Resources
For additional context, refer to:
- [REST API Authentication Mechanisms - Session Auth](https://www.example.com)
- [HTTP Cookies](https://developer.mozilla.org/en-US/docs/Web/HTTP/Cookies)
- [Flask Documentation](https://flask.palletsprojects.com/)

## Example Commands
To test your code:
```bash
python3 your_script.py
```
