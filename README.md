# Calis100 Backend

## Overview

This is the backend service for Calis100, a comprehensive calisthenics exercise tracking application. Built with Spring Boot, it provides RESTful API endpoints for user authentication, exercise logging, goal setting, and progress tracking, specifically tailored for calisthenics enthusiasts.

## Table of Contents

- [Features](#features)
- [Technologies](#technologies)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Running the Application](#running-the-application)
- [API Documentation](#api-documentation)
- [Database Schema](#database-schema)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication via Google Sign-In (OAuth2)
- CRUD operations for calisthenics exercises
- Goal setting and tracking for various calisthenics milestones
- Progress logging and visualization
- Customizable workout routines
- Performance analytics

## Technologies

- Java 17
- Spring Boot 3.1.x
- Spring Security (for OAuth2)
- MySQL 8.0
- Maven
- AWS SDK

## Prerequisites

Before you begin, ensure you have the following installed:
- JDK 17
- Maven 3.8+
- MySQL 8.0
- An IDE of your choice (IntelliJ IDEA recommended)

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/your-username/calis100-backend.git
   ```

2. Navigate to the project directory:
   ```
   cd calis100-backend
   ```

3. Create a MySQL database:
   ```sql
   CREATE DATABASE calis100;
   ```

4. Update `src/main/resources/application.properties` with your database credentials and OAuth2 configuration:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/calis100
   spring.datasource.username=your_username
   spring.datasource.password=your_password

   spring.security.oauth2.client.registration.google.client-id=your_google_client_id
   spring.security.oauth2.client.registration.google.client-secret=your_google_client_secret
   ```

5. Install dependencies:
   ```
   mvn clean install
   ```

## Running the Application

To run the application locally:

```
mvn spring-boot:run
```

The server will start on `http://localhost:8080`.

## API Documentation

API documentation is available at `http://localhost:8080/swagger-ui.html` when the application is running.

For detailed API documentation, refer to the [API Documentation](API_DOCUMENTATION.md) file.

## Database Schema

The database schema is managed using Flyway migrations. You can find the migration scripts in the `src/main/resources/db/migration` directory.

Key tables:
- `users`
- `exercises`
- `workouts`
- `goals`
- `progress`

## Testing

To run the tests:

```
mvn test
```

## Deployment

This application is designed to be deployed on AWS Elastic Beanstalk. Deployment instructions:

1. Package the application:
   ```
   mvn clean package
   ```

2. Deploy to Elastic Beanstalk using the AWS Management Console or the EB CLI.

For detailed deployment instructions, refer to the [Deployment Guide](DEPLOYMENT.md).

## Contributing

We welcome contributions to Calis100! Please read our [Contributing Guidelines](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
