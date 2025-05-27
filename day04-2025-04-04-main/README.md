# day04-2025-04-04
A Spring Boot application that provides REST endpoints to manage student data for lk.ac.vau.fas.ict.

## Overview

This application provides a RESTful API for performing CRUD (Create, Read, Update, Delete) operations on student records. The API allows users to:

- Retrieve student information
- Add new students
- Update existing student records
- Delete student records

## Project Structure

The project follows a standard Spring Boot structure:

```
src/
├── main/
│   ├── java/
│   │   └── lk/
│   │       └── ac/
│   │           └── vau/
│   │               └── fas/
│   │                   └── ict/
│   │                       ├── Controller/
│   │                       │   └── AppController.java
│   │                       └── model/
│   │                           └── Student.java
│   └── resources/
│       └── application.properties
```

## API Endpoints

### Basic Endpoints

- `GET /app/msg`: Returns a test message "Hello Spring Boot!"
- `GET /app/age/{ag}`: Returns a message with the provided age

### Student Endpoints

- `GET /app/student`: Returns a sample student object
- `GET /app/students`: Returns all students as a map with registration numbers as keys
- `GET /app/students/{rg}`: Returns a specific student by registration number
- `POST /app/add`: Adds a new student
- `DELETE /app/students/{id}`: Deletes a student by registration number
- `PUT /app/update/{id}`: Updates a student by registration number

## Student Model

The `Student` class has the following properties:

- `regNo`: Student registration number (unique identifier)
- `name`: Student name
- `age`: Student age
- `course`: student course
- `gpa`: Student grade point average

## Getting Started

### Prerequisites

- Java 8 or higher
- Maven or Gradle

### Running the Application

1. Clone the repository
2. Navigate to the project root directory
3. Run the application:

```bash
# Using Maven
mvn spring-boot:run

# Using Gradle
gradle bootRun
```

4. The application will start on the default port 8080

## API Usage Examples

### Get all students

```
GET http://localhost:8080/app/students
```

### Get a specific student

```
GET http://localhost:8080/app/students/2020ICT47
```
![Screenshot (1044)](https://github.com/user-attachments/assets/a641db9d-22e3-4a18-babe-5e6b0379d184)

### Add a new student

```
POST http://localhost:8080/app/add

```
![Screenshot (1051)](https://github.com/user-attachments/assets/e02d92f1-2b8f-40ca-9179-25cedb1b7b93)

![Screenshot (1045)](https://github.com/user-attachments/assets/1613f056-1645-4e43-b434-640c1404ae87)


### Update a student

```
PUT http://localhost:8080/app/update/2020ICT100
```
![Screenshot (1049)](https://github.com/user-attachments/assets/d17a4665-a051-4c46-b28c-40c7d59bc926)

![Screenshot (1050)](https://github.com/user-attachments/assets/22c1da91-9092-4cf2-a6fb-59500821e233)

### Delete a student

```
DELETE http://localhost:8080/app/students/2020CS31
```
![Screenshot (1046)](https://github.com/user-attachments/assets/50d10544-aa6c-4c48-a43e-7856c213455b)

![Screenshot (1047)](https://github.com/user-attachments/assets/eb081db4-9bae-4cb5-afad-a817176bf465)


