# Spring Boot JWT Authentication System

This repository provides a standardized, secure implementation of **JSON Web Token (JWT)** authentication for Spring Boot applications. It is designed to be a plug-and-play security module for microservices requiring stateless session management.

## Security Features

- **Stateless Authentication:** Uses JWTs to eliminate the need for server-side session storage.
- **Spring Security 6 Integration:** Leverages the latest Security Filter Chain configurations.
- **RBAC (Role-Based Access Control):** Pre-configured roles (e.g., `USER`, `ADMIN`) with method-level security.
- **Secure Password Storage:** Implementation of `BCryptPasswordEncoder`.
- **Token Lifecycle:** Custom logic for token generation, validation, and expiration handling.

## Architecture
1. **AuthenticationFilter:** Intercepts login requests and generates a JWT upon success.
2. **AuthorizationFilter:** Validates the JWT in the `Authorization` header for every protected request.
3. **SecurityConfig:** Defines public vs. private routes and entry points.

## Tech Stack
- **Framework:** Spring Boot 3.x
- **Security:** Spring Security 6.x
- **JWT Library:** `io.jsonwebtoken` (JJWT)
- **Database:** MySQL / PostgreSQL (JPA)

## Setup
1. Clone the repo.
2. Update `application.properties` with your database credentials and a secure `jwt.secret`.
3. Build and run: `mvn spring-boot:run`
