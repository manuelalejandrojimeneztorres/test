# SurveyHub Backend Server

[![Build Status](https://img.shields.io/badge/build-passing-brightgreen)](https://github.com/yourusername/SurveyHub/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Node.js Version](https://img.shields.io/badge/Node.js-%3E%3D16.x-brightgreen)](https://nodejs.org/)
[![MySQL Version](https://img.shields.io/badge/MySQL-8.x-orange)](https://www.mysql.com/)

SurveyHub is a robust backend application designed to support the SurveyHub system, a comprehensive platform for managing online surveys. This server provides secure, scalable, and efficient APIs for handling survey operations, user authentication, and data management.

---

## Table of Contents

1. [Introduction](#introduction)
2. [Features](#features)
3. [Prerequisites](#prerequisites)
4. [Installation](#installation)
   - [Clone the Repository](#1-clone-the-repository)
   - [Install Dependencies](#2-install-dependencies)
   - [Database Setup](#3-database-setup)
   - [Environment Configuration](#4-environment-configuration)
   - [Start the Server](#5-start-the-server)
5. [Usage](#usage)
6. [Built With (Tools and Technologies)](#built-with-tools-and-technologies)
7. [Dependencies](#dependencies)
8. [Contributing](#contributing)
9. [License](#license)
10. [Acknowledgments](#acknowledgments)

---

## Introduction

The **SurveyHub Backend Server** provides RESTful APIs for creating, managing, and analyzing surveys. Designed using modern frameworks and tools, this server ensures high performance, security, and maintainability, making it a reliable backbone for enterprise-level survey management systems.

---

## Features

- **Role-Based Access Control (RBAC):** Admin and user roles with tailored access.
- **Secure Authentication:** Powered by JWT and bcrypt.
- **Survey Management:** APIs for creating, updating, and deleting surveys.
- **Data Insights:** Efficient data retrieval for analytics.
- **Scalable Architecture:** Designed for horizontal and vertical scalability.
- **API Documentation:** Comprehensive OpenAPI 3.0.3 documentation for developers.

---

## Prerequisites

Ensure the following tools are installed on your system:

- [Node.js (>=16.x)](https://nodejs.org/)
- [MySQL Server (>=8.x)](https://dev.mysql.com/downloads/)
- [Git](https://git-scm.com/downloads)
- **Optional:**
  - [Postman](https://www.postman.com/) or any REST API client for testing APIs.

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/SurveyHub.git
cd SurveyHub/backend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Database Setup

Ensure MySQL is running. Create a database named `surveyhub`:

```sql
CREATE DATABASE surveyhub;
```

### 4. Environment Configuration

Create a `.env` file in the `backend` directory:

```env
NODE_ENV=development
PORT=8080
DB_HOST=localhost
DB_PORT=3306
DB_USER=root
DB_PASSWORD=YourStrongPassword
DB_NAME=surveyhub
JWT_SECRET=YourJWTSecret
```

### 5. Start the Server

Run the development server:

```bash
npm start
```

The server will be available at `http://localhost:8080`.

---

## Usage

- Access the API documentation at `http://localhost:8080/api-docs` (OpenAPI 3.0.3).
- Use Postman or any REST client to test the endpoints.
- Example of retrieving all surveys:
  ```bash
  GET /surveys
  ```
  Response:
  ```json
  [
    {
      "id": 1,
      "name": "Customer Feedback",
      "description": "Survey for gathering customer insights.",
      "startDate": "2024-01-01T00:00:00.000Z",
      "status": "Active"
    }
  ]
  ```

---

## Built With (Tools and Technologies)

- **Backend Framework:** Node.js, Express.js
- **Database Management:** MySQL, Sequelize ORM
- **Authentication:** bcrypt, jsonwebtoken
- **Environment Management:** dotenv
- **Logging:** Logback
- **API Documentation:** OpenAPI 3.0.3 (Swagger)

---

## Dependencies

Below is a list of major dependencies used in the project:

- **Express.js**: Fast and minimalist web framework.
- **Sequelize**: ORM for MySQL database interaction.
- **jsonwebtoken**: For secure authentication.
- **bcrypt**: For hashing user passwords.
- **dotenv**: For managing environment variables.

For the complete list, refer to `package.json`.

---

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Description of changes"`.
4. Push to the branch: `git push origin feature-name`.
5. Create a pull request.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **Node.js and Express.js Teams**: For their exceptional tools.
- **Sequelize Contributors**: For simplifying database operations.
- **OpenAPI Initiative**: For promoting standardized API documentation.
- **GitHub Community**: For continuous support and inspiration.

---

Enjoy developing with **SurveyHub Backend Server**! 🚀
