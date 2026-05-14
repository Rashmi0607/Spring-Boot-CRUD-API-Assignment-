# Spring Boot CRUD API with Authentication & File Upload

## Features

### Authentication Service

* User Registration
* User Login
* JWT Authentication

### Details Service

Secured CRUD APIs for:

* Name
* Email
* Country Code + Phone
* Address
* PDF Upload
* Video Upload

### Security

* Spring Security
* JWT Token Authentication
* Protected Routes

### Architecture

* Controller
* Service
* Repository
* DTO/Payload Classes

---

# Tech Stack

* Java
* Spring Boot
* Spring Security
* JWT
* Spring Data JPA
* MySQL
* Maven

---

# Authentication APIs

## Register

POST `/api/auth/register`

```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

## Login

POST `/api/auth/login`

```json
{
  "email": "user@gmail.com",
  "password": "123456"
}
```

Response:

```json
{
  "token": "JWT_TOKEN"
}
```

---

# Details APIs

Use JWT token in Authorization Header:

Bearer YOUR_TOKEN

## Create Details

POST `/api/details`

## Get All Details

GET `/api/details`

## Get Details By ID

GET `/api/details/{id}`

## Update Details

PUT `/api/details/{id}`

## Delete Details

DELETE `/api/details/{id}`

---

# Configure Database

Update `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/your_db
spring.datasource.username=root
spring.datasource.password=Rashmihv@100
``

---

# Run Project

## Install Dependencies

```bash
mvn clean install
```

## Start Application

```bash
mvn spring-boot:run
```

---

# Project Structure

src
└── main
└── java
└── com.example
├── controller
├── service
├── repository
├── dto
├── entity
├── security
└── config

---

# Security Features

* JWT Authentication
* BCrypt Password Encryption
* Protected APIs
