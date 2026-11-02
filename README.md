# Employee Management API

A RESTful employee management service built with Java 17 and Spring Boot. It demonstrates layered application design, REST endpoints, persistence with Spring Data JPA, request validation, and centralized exception handling.

## Technology stack

- Java 17
- Spring Boot 3.3.5
- Spring Web
- Spring Data JPA
- H2 in-memory database
- Jakarta Bean Validation
- Maven
- JUnit 5 / Spring Boot Test

## Features

- Create an employee
- List all employees
- Retrieve an employee by ID
- Update an employee
- Delete an employee
- Validate required fields, email format, and non-negative salary
- Reject duplicate email addresses
- Return structured error responses

## Prerequisites

- JDK 17 or newer
- Maven 3.6+ (or use the Maven wrapper if you add one)

## Run locally

```bash
mvn spring-boot:run
```

The API starts at `http://localhost:8080`.

## API endpoints

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/employees` | Create an employee |
| GET | `/api/employees` | List employees |
| GET | `/api/employees/{id}` | Get employee by ID |
| PUT | `/api/employees/{id}` | Update employee |
| DELETE | `/api/employees/{id}` | Delete employee |

## Example request

`POST /api/employees`

```json
{
  "firstName": "Jordan",
  "lastName": "Lee",
  "email": "jordan.lee@example.com",
  "department": "Engineering",
  "salary": 85000
}
```

## Run tests

```bash
mvn test
```

## Database

This starter project uses an in-memory H2 database. Data is reset when the application stops. The H2 console is available at `http://localhost:8080/h2-console` while the app is running.

JDBC URL: `jdbc:h2:mem:employeedb`  
Username: `sa`  
Password: (blank)

## Project structure

```text
src/main/java/com/example/employee/
├── controller/  # HTTP endpoints
├── exception/   # API error handling
├── model/       # JPA entity
├── repository/  # Database access
└── service/     # Business logic
```

## Future improvements

- Add pagination and sorting
- Add DTOs and MapStruct
- Add integration tests for CRUD endpoints
- Replace H2 with PostgreSQL or MySQL for persistent storage
- Add Spring Security and role-based access control
- Add Docker support and CI with GitHub Actions

## Author

Add your name and GitHub profile URL here.
