# Library API

A RESTful API for managing books, built with Spring Boot and MySQL.

## Tech Stack

- **Java 21**
- **Spring Boot 4.1.2**
- **Spring Data JPA** – ORM and data access
- **MySQL** – Relational database
- **Bean Validation** – Request validation
- **SpringDoc OpenAPI** – Swagger UI documentation

## API Endpoints

| Method | Endpoint | Description |
|--------|-------------------|---------------------|
| GET | `/api/books` | Get all books |
| GET | `/api/books/{id}` | Get a book by ID |
| POST | `/api/books` | Create a new book |
| PUT | `/api/books/{id}` | Update a book by ID |
| DELETE | `/api/books/{id}` | Delete a book by ID |

## Getting Started

### Prerequisites

- Java 21+
- MySQL Server
- Maven (or use the included Maven wrapper)

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/ImeshMunasinghe/EAD_Lab.git
   cd EAD_Lab
   ```

2. **Create the MySQL database**
   ```sql
   CREATE DATABASE library_db;
   ```

3. **Configure environment variables**

   Copy the example env file and fill in your database credentials:
   ```bash
   cp .env.example .env
   ```
   Edit `.env`:
   ```env
   DB_URL=jdbc:mysql://localhost:3306/library_db
   DB_USERNAME=root
   DB_PASSWORD=your_database_password
   ```

4. **Run the application**
   ```bash
   ./mvnw spring-boot:run
   ```

5. **Access the API**
   - API base URL: `http://localhost:8080/api/books`
   - Swagger UI: `http://localhost:8080/swagger-ui/index.html`

## Project Structure

```
src/main/java/lk/ac/mrt/fit/library_api/
├── LibraryApiApplication.java      # Entry point with .env loader
├── controller/
│   └── BookController.java         # REST controller
├── model/
│   └── Book.java                   # JPA entity
├── repository/
│   └── BookRepository.java         # Data access layer
└── service/
    └── BookService.java            # Business logic
```
