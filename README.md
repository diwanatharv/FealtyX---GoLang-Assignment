# Student API

This is a simple REST API built with Go to perform CRUD operations on a list of students. Each student has the following attributes:
- ID (integer)
- Name (string)
- Age (integer)
- Email (string)

Additionally, it integrates with Ollama to generate AI-based responses for certain actions.

## Endpoints

- **Create a new student**: `POST /students`
- **Get all students**: `GET /students`
- **Get a student by ID**: `GET /students/{id}`
- **Update a student by ID**: `PUT /students/{id}`
- **Delete a student by ID**: `DELETE /students/{id}`
- **Generate a summary of a student by ID using Ollama**: `GET /students/{id}/summary`

## Run the API

To run the API, follow these steps:

1. Clone the repository.
2. Navigate to the project directory.
3. Initialize Go modules: `go mod init student-api`
4. Install required packages: `go get -u github.com/gorilla/mux` and `go get -u github.com/gorilla/handlers`
5. Run the application: `go run main.go`

The server will start on `http://localhost:8080`.

## Example Requests

### Create a New Student

```sh
curl -X POST http://localhost:8080/students -H "Content-Type: application/json" -d '{
    "name": "John Doe",
    "age": 20,
    "email": "john.doe@example.com"
}'
