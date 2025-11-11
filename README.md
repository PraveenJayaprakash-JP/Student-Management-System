# Student Management System

A comprehensive web application for managing student records with CRUD operations, built using Spring Boot, REST API, and MySQL.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Database Schema](#database-schema)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

The Student Management System is a RESTful web application that provides a complete solution for managing student information. It follows the MVC (Model-View-Controller) architecture pattern and implements CRUD (Create, Read, Update, Delete) operations through REST APIs.

## ✨ Features

- ✅ Create new student records
- ✅ View all students
- ✅ View individual student details
- ✅ Update student information
- ✅ Delete student records
- ✅ RESTful API architecture
- ✅ MySQL database integration
- ✅ Spring Data JPA for data persistence
- ✅ Lombok for reducing boilerplate code

## 🛠️ Technologies Used

### Backend
- **Spring Boot 3.5.7** - Application framework
- **Spring Data JPA** - Data persistence and ORM
- **Spring Web** - RESTful web services
- **MySQL** - Relational database
- **Lombok** - Reducing boilerplate code
- **Maven** - Dependency management and build tool

### Tools
- **Spring Boot DevTools** - Development productivity
- **Java 17** - Programming language

## 📁 Project Structure

```
Student-Management-System/
├── src/
│   ├── main/
│   │   ├── java/in/entireskill/sms/
│   │   │   ├── controller/         # REST controllers
│   │   │   ├── model/              # Entity classes
│   │   │   ├── repository/         # JPA repositories
│   │   │   ├── service/            # Business logic
│   │   │   └── StudentManagementSystemApplication.java
│   │   └── resources/
│   │       └── application.properties
│   └── test/                       # Test classes
├── target/                         # Compiled files
├── pom.xml                         # Maven configuration
├── mvnw                            # Maven wrapper script (Unix)
├── mvnw.cmd                        # Maven wrapper script (Windows)
└── README.md
```

## 📋 Prerequisites

Before running this application, make sure you have:

- **JDK 17** or higher installed
- **MySQL Server** installed and running
- **Maven 3.6+** (or use the included Maven wrapper)
- **Git** (for cloning the repository)

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/PraveenJayaprakash-JP/Student-Management-System.git
cd Student-Management-System
```

### 2. Create MySQL Database

Login to MySQL and create a database:

```sql
mysql -u root -p
CREATE DATABASE student_management;
EXIT;
```

## ⚙️ Configuration

Update the `src/main/resources/application.properties` file with your MySQL credentials:

```properties
# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/student_management
spring.datasource.username=your_mysql_username
spring.datasource.password=your_mysql_password

# JPA/Hibernate Configuration
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect

# Server Configuration
server.port=8080
```

## ▶️ Running the Application

### Using Maven Wrapper (Recommended)

**On Windows:**
```bash
mvnw.cmd spring-boot:run
```

**On Unix/Mac:**
```bash
./mvnw spring-boot:run
```

### Using Maven

```bash
mvn spring-boot:run
```

### Using JAR File

```bash
mvn clean package
java -jar target/StudentManagementSystem-0.0.1-SNAPSHOT.jar
```

The application will start on `http://localhost:8080`

## 🔌 API Endpoints

Here are the main REST API endpoints:

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/students` | Get all students |
| GET | `/api/students/{id}` | Get student by ID |
| POST | `/api/students` | Create new student |
| PUT | `/api/students/{id}` | Update student |
| DELETE | `/api/students/{id}` | Delete student |

### Sample Request/Response

**POST /api/students**

```json
{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com",
  "department": "Computer Science",
  "yearOfEnrollment": 2024
}
```

**Response:**

```json
{
  "id": 1,
  "firstName": "John",
  "lastName": "Doe",
  "email": "john.doe@example.com",
  "department": "Computer Science",
  "yearOfEnrollment": 2024
}
```

## 🗃️ Database Schema

The application uses a `students` table with the following structure:

| Column | Type | Constraints |
|--------|------|-------------|
| id | BIGINT | PRIMARY KEY, AUTO_INCREMENT |
| first_name | VARCHAR(255) | NOT NULL |
| last_name | VARCHAR(255) | NOT NULL |
| email | VARCHAR(255) | UNIQUE, NOT NULL |
| department | VARCHAR(255) | |
| year_of_enrollment | INT | |

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Praveen Jayaprakash**

- GitHub: [@PraveenJayaprakash-JP](https://github.com/PraveenJayaprakash-JP)

## 📧 Contact

For any queries or suggestions, feel free to reach out or create an issue in the repository.

---

⭐ If you found this project helpful, please give it a star!
