# API Key Management with Spring Boot

This project demonstrates API key-based authentication using Spring Boot and Spring Security.

## Setup

1. **Clone the repository** and configure the MySQL database in `application.properties`.
2. **Run the application** using your IDE or with `mvn spring-boot:run`.

## Endpoints

### Public Endpoints

- **`GET /public/hello`**: Returns a greeting message. No authentication required.

- **`GET /public/generate-default-company`**: Creates a dummy company and client, and generates an API key. Use this endpoint to initialize the system.

### Protected Endpoints

- **`GET /protected`**: A protected endpoint that requires a valid API key.

## Testing

1. **Generate Company and Client**:
    - Request: `GET /public/generate-default-company`
    - This will return an API key for the created client.

2. **Access Protected Endpoint**:
    - Request: `GET /protected`
    - Add the API key to the header: `x-api-key: YOUR_API_KEY`

## Summary

- **Public endpoints** are accessible without authentication.
- **Protected endpoints** require API key validation.
