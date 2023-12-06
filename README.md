# go-bookstore: RESTful API for Book Management

This GitHub repository hosts the Go-Bookstore project, a RESTful API built with Go for managing a bookstore. It features a MySQL database for persistent storage and uses the GORM library for object-relational mapping.

## Features

- **RESTful API:** Provides endpoints for creating, retrieving, updating, and deleting books.
- **MySQL Database Integration:** Uses MySQL for storing book data.
- **GORM Integration:** Leverages GORM for database operations.

## Getting Started

### Prerequisites

- Go 1.x or later
- MySQL

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/ay-bh/go-bookstore.git
   ```
2. Navigate to the project directory:
   ```bash
   cd go-bookstore
   ```

### Running the Application

1. Set up your MySQL database and update the connection details in `config.go`.
2. Run the application:
   ```bash
   go run cmd/main.go
   ```

## API Endpoints

The application exposes several endpoints for managing books:

- **Create Book:** `POST /books`
- **Get All Books:** `GET /books`
- **Get Book By ID:** `GET /books/{id}`
- **Update Book:** `PUT /books/{id}`
- **Delete Book:** `DELETE /books/{id}`

## Book Model

The `Book` model is defined as follows:

```go
type Book struct {
    gorm.Model
    Name        string `json:"name"`
    Author      string `json:"author"`
    Publication string `json:"publication"`
}
```
