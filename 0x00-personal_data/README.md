# 0x00. Personal Data - Backend Authentication

This project implements secure handling of personal data in a backend application using Python and MySQL. It covers essential techniques in data logging, PII protection, password encryption, and secure database access.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Project Structure](#project-structure)
4. [Setup and Installation](#setup-and-installation)
5. [Usage](#usage)
6. [Tasks Overview](#tasks-overview)

---

### Project Overview
The main objectives of this project are to:
- Identify and manage Personally Identifiable Information (PII)
- Obfuscate sensitive data in log files using regex and custom formatting
- Securely authenticate and connect to a database using environment variables
- Encrypt passwords and validate user authentication securely

---

### Features
- **Logging with Obfuscation**: Utilizes a custom logging filter to hide sensitive data in logs.
- **PII Field Identification**: Defines key fields to mask for privacy.
- **Secure Database Connection**: Connects to a MySQL database using environment variables for credentials.
- **Password Encryption**: Encrypts and validates passwords using the `bcrypt` library.

---

### Project Structure
```plaintext
0x00-personal_data/
├── filtered_logger.py    # Main module with logging and PII management
├── README.md             # Project documentation (this file)
├── user_data.csv         # Example data file with user information
└── main.py               # Script to demonstrate functionality
```

---

### Setup and Installation

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/alx-backend-user-data.git
    cd 0x00-personal_data
    ```

2. **Install Dependencies**:
    - **Python 3.7**
    - Install required packages:
      ```bash
      pip install bcrypt mysql-connector-python
      ```

3. **Database Setup**:
    Set up your MySQL database:
    ```sql
    CREATE DATABASE IF NOT EXISTS my_db;
    CREATE USER IF NOT EXISTS 'root'@'localhost' IDENTIFIED BY 'root';
    GRANT ALL PRIVILEGES ON my_db.* TO 'root'@'localhost';

    USE my_db;
    -- Create the users table as shown in the example SQL setup
    ```

4. **Environment Variables**:
    Export database credentials to environment variables:
    ```bash
    export PERSONAL_DATA_DB_USERNAME="root"
    export PERSONAL_DATA_DB_PASSWORD="root"
    export PERSONAL_DATA_DB_HOST="localhost"
    export PERSONAL_DATA_DB_NAME="my_db"
    ```

---

### Usage

To execute the project, run the following:
```bash
python3 main.py
```
This will demonstrate logging obfuscation, database connection, and filtered data display.

---

### Tasks Overview

1. **Regex-ing**: Obfuscates PII fields in log messages using regex.
2. **Log Formatter**: Custom `RedactingFormatter` class to format log records with masked fields.
3. **Create Logger**: Configures a secure logger that hides sensitive information.
4. **Database Connection**: Securely connects to a MySQL database using environment variables.
5. **Read and Filter Data**: Reads data from the `users` table, filtering and logging it in a secure format.

---

For detailed information on each feature, see inline comments and function docstrings in the `filtered_logger.py` file. 

**Enjoy coding securely!**
