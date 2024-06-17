# File Upload Service

This project is a REST service for uploading files and displaying a list of already uploaded files by the user. All requests to the service must be authorized. The service is designed to integrate with a pre-prepared web application (FRONT) without modifications and use the FRONT functionality for authorization, file upload, and file list display.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Setup](#setup)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Testing](#testing)
- [Docker](#docker)
- [Contributing](#contributing)
- [License](#license)

## Features

- REST interface for integration with FRONT
- List files
- Add files
- Delete files
- User registration and authentication
- Settings loaded from a configuration file (YAML)
- User information and data stored in a database

## Technologies

- Java
- Spring Boot
- Spring Security
- JPA/Hibernate
- Docker
- Testcontainers
- JUnit
- Mockito

## Setup

### Prerequisites

- Java 11 or later
- Docker and Docker Compose

### Installation

1. Clone the repository:
   
    git clone https://github.com/yourusername/file-upload-service.git
    cd file-upload-service
    
2. Build the project:
   
    ./mvnw clean install
    
3. Run the application:
   
    ./mvnw spring-boot:run
    
### Docker

To run the application using Docker and Docker Compose:

1. Build and start the containers:
   
    docker-compose up --build
    
The application should now be running at http://localhost:8080.

## Usage

1. Register a new user via the /api/users/register endpoint.
2. Authenticate and obtain a token.
3. Use the token to upload files and list the uploaded files.

## API Endpoints

- POST /api/users/register - Register a new user
- POST /api/files - Upload a file
- GET /api/files - List files
- DELETE /api/files/{id} - Delete a file

## Testing

### Unit Tests

To run unit tests using Mockito:

```sh
./mvnw test

To run integrations tests

./mvnw integration-test
